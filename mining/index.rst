
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


POS Mining
==========

This documentation describes how to mine MarteX under the Windows
operating system using just your computer. Please note that
the you will need a unlock wallet with minimum of 5 MXT running 24 h.

Mining software
---------------

The first step is to download the MarteXcore because all mine process occurs there.


Configuration
-------------

You need a

Testing
-------



Masternode Mining
=================

You need to create a `masternode <~/masternode>`_ to mine.
