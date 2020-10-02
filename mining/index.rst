
.. meta::
   :description: Information and guides on how to mine the MarteX cryptocurrency
   :keywords: martex, mining, X13, masternode, software, hardware, Proof of Stake (PoS)

.. _mining:

======
Mining
======

Mining in the context of cryptocurrency such as MarteX refers to the
process of placing your coin as collateral - if you're trying to promote invalid
transactions when it's your turn to validate the next block, you will lose a portion of your stake. The process of mining creates new currency tokens as a reward to the miner. Mining is possible on any hardware running MarteXcore. MarteX implements an algorithm known as `X13 <https://github.com/martexcoin/coinhash>`_, which gives more security to the network in case of attack.

The result is a currency which is more
secure against brute force attacks on the MarteX blockchain.

The simplest and most general hardware available for mining is the minimum hardware requirements listed bellow:

- 1 CPU.
- 1024 MB of free RAM and 1024 of Swap.
- 4 GB of free storage (The more the blockchain grows, the more storage is needed).
- A good internet connection (The more transactions are made, the more connection is needed).

The profitability of mining is determined by the current network difficulty,
the costs of your hardware, electricity, how many coin do you have, how long is your MarteXcore online.
The following link provide up to date information:
`GetDIfiiculty <https://be.martexcoin.org/api/getdifficulty>`_



Masternodes vs. Mining
======================

MarteX, like Bitcoin and most other cryptocurrencies, is based on a
decentralized ledger of all transactions, known as a blockchain. This
blockchain is secured through a consensus mechanism; in the case of 
Bitcoin, the consensus mechanism is Proof of Work (PoW). 
In the other hand, the consensus mechanism of MarteX is Proof of Stake `(PoS) <https://en.bitcoinwiki.org/wiki/Proof-of-stake>`_
. 
Where consensus is achieved by requiring users to stake an amount of their tokens so as to have a chance of being selected to validate blocks of transactions, and get rewarded for doing so.

Moreover, MarteX works a little differently from Bitcoin, however, because it has a
two-tier network. The second tier is powered by `Masternode </masternode>`_ (Full Nodes), which enable financial privacy (AnonSend), 
instant transactions (FastSend), and the decentralized
governance and budget system. Because this second tier is so important,
masternodes are also rewarded when miners discover new blocks. The
breakdown is as follows: 45% of the block reward goes to the miner, 45%
goes to masternodes, and 10% is reserved for the budget system (created
by `superblocks <https://martexcoin.org/governance/>`_).

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

- The first step is to download the MarteXcore because all mining process occurs there.
- Wait MarteXcore to fully sync.
- Send the minimum of 5 MXT to a wallet in your MarteXcore.
- Unlock your wallet (if it was locked) and leave your computer running 24h with an adequate internet connection. 


Configuration
-------------

You do not need to configure your wallet.

Testing
-------

You can test it using the `test network </testing>`_.

Masternode Mining
=================

You need to create a `masternode </masternode>`_ to mine.
