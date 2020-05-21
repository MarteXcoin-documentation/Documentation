
.. meta::
   :description: Information and guides on how to mine the MarteX cryptocurrency
   :keywords: martex, mining, X13, masternode, software, hardware

.. _mining:

======
Mining
======

Mining in the context of cryptocurrency such as MarteX refers to the
process of searching for solutions to cryptographically difficult
problems as a method of securing blocks on the blockchain. The process
of mining creates new currency tokens as a reward to the miner. Mining
is possible on a range of hardware. MarteX implements an algorithm known
as `X13 <https://github.com/martexcoin/coinhash>`_, which the miner must solve in order to earn rewards.

The simplest and most general hardware available for mining is the
general purpose CPU present in every computer. 
uneconomic due to the increased difficulty of hashing arising from the
rapidly increasing hash rate. The result is a currency which is more
secure against brute force attacks on the Dash blockchain.

The profitability of mining is determined by the hashrate of your mining
device, the current network difficulty and the costs of your hardware
and electricity. The following links provide up to date information:


Masternodes vs. Mining
======================

MarteX, like Bitcoin and most other cryptocurrencies, is based on a
decentralized ledger of all transactions, known as a blockchain. This
blockchain is secured through a consensus mechanism; in the case of 
Bitcoin, the consensus mechanism is Proof of Work (PoW). 
The consensus mechanism of MarteX is Proof of Stake (PoS). 
Miners attempt to solve difficult problems with how many coins he had in a  computers, and when
they solve the problem, they receive the right to add a new block to the
blockchain. If all the other people running the software agree that the
problem was solved correctly, the block is added to the blockchain and
the miner is rewarded.

But MarteX works a little differently from Bitcoin, however, because it has a
two-tier network. The second tier is powered by [Masternodes](~/masternode) (Full Nodes), which enable financial privacy
(AnonSend), instant transactions (FastSend), and the decentralized
governance and budget system. Because this second tier is so important,
masternodes are also rewarded when miners discover new blocks. The
breakdown is as follows: 45% of the block reward goes to the miner, 45%
goes to masternodes, and 10% is reserved for the budget system (created
by superblocks every month).

The masternode system is referred to as Proof of Service (PoSe), since
the masternodes provide crucial services to the network. In fact, the
entire network is overseen by the masternodes, which have the power to
reject improperly formed blocks from miners. If a miner tried to take
the entire block reward for themselves or tried to run an old version of
the MarteX software, the masternode network would orphan that block, and
it would not be added to the blockchain.

In short, miners power the first tier, which is the basic sending and
receiving of funds and prevention of doublespending. Masternodes power
the second tier, which provide the added features that make MarteX
different from other cryptocurrencies. Masternodes do not mine, and
mining computers cannot serve as masternodes. Additionally, each
masternode is “secured” by 5000 MARTEX. Those MARTEX remain under the sole
control of their owner at all times, and can still be freely spent. The
funds are not locked in any way. However, if the funds are moved or
spent, the associated masternode will go offline and stop receiving
rewards.


CPU Mining
==========

This documentation describes how to mine Dash under the Windows
operating system using just the CPU in your computer. Please note that
the prevalence of GPU and ASIC miners mean that unless you have free
electricity, this is highly unlikely to be profitable! Since this is the
case, the software in this guide has not been updated in several years,
and is intended for experimental purposes and testnet only.

This is a fairly simple procedure and examples will be given in order to
achieve the fastest possible hash rate for your CPU, but remember that
more optimized miners do exist, so we advise you to keep an eye out on
mining sites such as these in order to keep up with the latest
information and releases.

- `Crypto Mining Blog <http://cryptomining-blog.com/>`_
- `Dash Forum Mining Discussions <https://www.dash.org/forum/topic/mining.3/>`_
- `Bitcoin Talk Altcoin Mining Discussions <https://bitcointalk.org/index.php?board=160.0>`_

Mining software
---------------

The first step is to download appropriate mining software. A good basic
miner for modern CPUs can be found here:



Configuration
-------------

Begin by selecting a mining pool and generating a Dash address as
described in the :ref:`Mining Pools <mining-pools>` section above. Keep
all your mining files in a single folder. In this example we will work
from the Desktop. The node selected for this example is from the
p2poolming.us list and is located in China::

  http://118.184.180.43:7903/static/

Next, open **Notepad** and type in on one line the command we will use
to start the miner, followed by pause on the second line. The general
format is as follows::

  <minerd> -a <algorithm> -o <url> -u <username> -p <password> -t <threads>
  pause

Where:

- minerd = the executable miner daemon file you choose to use
- a = algorithm, which is X11 for Dash
- o = URL of your mining pool, including the protocol and port
- u = username, usually the Dash receiving address of your wallet or worker
- p = password, can often be set to x
- t = number of threads used
- pause = keeps the window open in the case of errors

For the CPU in the example above, the command may be::

  minerd-avx-aes-sse2-sss3.exe -a X11 -o stratum+tcp://118.184.180.43:7903 -u XwZRjo1f6gmq3LCv7X1Hi5h3NkvDMHvu8G -p x -t 8
  pause

.. figure:: img/notepad.png
   :width: 400px

   Notepad file showing an example command to start a CPU miner

Click **File**, then **Save As**. Change **Save as type** to **All
Files**, then type the file name as *startminer.bat* and save it in the
same folder as the unzipped *minerd* files.

Testing
-------



GPU Mining
==========



Mining software
---------------

As for CPU mining, a range of mining software is available for GPU
mining. Most of it based on sgminer compiled with different
optimizations specific to different hardware. A good approach is to
identify your graphics hardware, then choose an appropriate build of
sgminer. You can use `GPU-Z <https://www.techpowerup.com/gpuz/>`_ to
identify your GPU hardware:

.. figure:: img/gpu-z.png
   :width: 400px

   GPU-Z showing details for AMD Radeon Turks and NVIDIA Quadro GK104
   class GPUs

Next, download the mining software. Most of these are based on the
original `sgminer <https://github.com/sgminer-dev/sgminer>`_, but this
is not suitable for the X11 algorithm, offers no compiled binaries and
hasn't been updated in years. We will describe using pre-compiled binary
software maintained by newer developers only.

**AMD**

- https://github.com/nicehash/sgminer/releases

**NVIDIA**

- https://github.com/tpruvot/ccminer/releases (focus on core 
  application)
- https://github.com/sp-hash/ccminer/releases (sp-mod, optimized CUDA
  kernels for Windows)
- https://github.com/KlausT/ccminer/releases (similar to SP version,
  more clean)

Download your chosen release and extract the zip file to a known
location. The folder should look something like this:

.. figure:: img/gpu-miner-files.png
   :width: 400px

   Executable GPU miners for Dash

The sgminer file is the executable file, while the various files with
.cl extensions define the various algorithms supported by sgminer. In
this case, we are interested in the darkcoin.cl and darkcoin-mod.cl
implementations of X11. Note that the name of the executable file may be
different for miners with different optimizations, for example ccminer
for NVIDIA cards.

Configuration
-------------

Begin by selecting a mining pool and generating a Dash address as
described in the :ref:`Mining Pools <mining-pools>` section above. Keep
all your mining files in a single folder. In this example we will work
from the Desktop. The node selected for this example is from the
p2poolming.us list and is located in China::

  http://118.184.180.43:7903/static/

Next, open **Notepad** and create the basic configuration. The general
format is as follows::

  {
    "pools" : [
      {
        "url" : "stratum+tcp://pooladdress:7903",
        "user" : "walletaddress",
        "pass" : "x",
        "algorithm":"darkcoin"
      }
    ]
  }

Where:

- pools = defines a list of pools (in this case, only one) towards which
  the hashing power is directed
- url = URL of your mining pool, including the protocol and port
- user = username, usually the Dash receiving address of your wallet or
  worker
- pass = password, can often be set to x
- algorithm = hashing algorithm to use, in this case darkcoin (for
  historic reasons) or darkcoin-mod

For the pool above, the configuration may be:

.. figure:: img/gpu-config.png
   :width: 400px

   Configuration file for a Dash GPU miner

Click **File**, then **Save As**. Change **Save as type** to **All
Files**, then type the file name as *sgminer.conf* and save it in the
same folder as the unzipped *sgminer* files.
