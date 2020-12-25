.. meta::
   :description: Practical guide to using the MarteX governance system and treasury
   :keywords: martex, dgbb, governance, funding, voting, proposals, masternodes

.. _using-governance:

=====================
Using MarteX Governance
=====================

MarteX's Decentralized Governance by Blockchain (DGBB) is a novel voting
and funding platform. This documentation introduces and details the
theory and practice to use the system.

Understanding the process
=========================

Introduction
------------

- DGBB consists of three components: Proposals, Votes, and Budgets
- Anyone can submit a proposal for a small fee
- Each valid masternode can vote for, against or abstain on proposals
- Approved proposals become budgets
- Budgets are paid directly from the blockchain to the proposal owner

Proposals
---------

- Proposals are a request to receive funds
- Proposals can be submitted by anyone for a fee of 5 MarteX. The proposal
  fee is irreversibly destroyed on submission.
- Proposals cannot be altered once submitted

Votes
-----

- Votes are cast using the registered voting address
- The voting address can be delegated to a third party
- Votes can be changed at any time
- Votes are counted every 16616 blocks (approx. 30.29 days)

Budgets
-------

- Budgets are proposals which receive a net total of yes votes equal to
  or greater than 10% of the total possible votes (for example over 448
  out of 4480)
- Budgets can be nullified at any time if vote totals (cast or re-cast)
  fall below the approval threshold
- Budgets are processed (paid) in order of yes minus no votes. More
  popular budgets get payment priority. 
- Approximately 6176 martex (in 2018) are available for each budget cycle,
  decreasing by 7.14% every 210240 blocks (approx. 383.25 days).

Object structure
----------------

The following information is required to create a proposal:

- end_epoch: TIMESTAMP UTC / MAXIMUM PROJECT DATE (numeric)
- name: "lowercase project name (up to 20 characters)" (string)
- payment_address: "WALLET ADDRESS" (string)
- payment_amount: QTY OF MXT TO BE COLLECTED (numeric)
- start_epoch: TIMESTAMP UTC / CURRENT DATE OR NEXT SUPERBLOCK (numeric)
- type: 1 (always)
- url: "PROJECT SITE / DOCUMENT" (string)

Persistence
-----------

- Proposals become active one day after submission
- Proposals will remain visible on the network until they are either
  disapproved or the proposal's last payment-cycle is reached
- Approval occurs when yes votes minus no votes equals 10% or more of
  the total available votes.
- Disapproval occurs when no votes minus yes votes equals 10% or more of
  the total available votes.
- The total available votes is the count of online and responding
  masternodes and can be seen by running the command 
  ``masternode count`` in the MarteX Core wallet debug window.

Templates
---------

The following one Microsoft Word template are available from MarteX Core
Group to help facilitate standardized proposal submission and updates.
Usage is recommended, but not required.

- `Project Proposal Template <https://github.com/martexcoin/proposal>`_

Budget cycles
=============

When preparing a proposal, be aware of when the next cycle will occur
and plan accordingly. It is recommended to choose your proposal payment
start block at least one cycle in the future to allow time for
discussion and gathering support and votes. Note that votes will no
longer be tallied 1662 blocks (approximately 32 minutes) prior to the
superblock.

.. _creating-proposals:

Creating proposals
==================

Once you have prepared the text of your proposal and set up a website or
forum post, it is time to submit your proposal to the blockchain for
voting. All tasks involved with creating a budget proposal can be
executed from the MarteX Core wallet console.

- `All the steps to generate a proposal can be found here. <https://github.com/martexcoin/proposal>`_

Voting on proposals
===================

**You must vote at least 32 minutes before the superblock is created or
your vote will not be counted. The exact deadline is 1662 blocks before
the superblock.**

Voting on DGBB proposals is an important part of operating a masternode.
Since masternodes are heavily invested in MarteX, they are expected to
critically appraise proposals each month and vote in a manner they
perceive to be consistent with the best interests of the network. Each
masternode may vote once on each proposal, and the vote can be changed
at any time before the voting deadline. The following sites and tools
are available to view and manage proposals and voting:

- `MarteXcore governance <https://martexcoin.org/governance/>`_

For information on how to create a proposal, see `here. <#creating-proposals>`_

.. _martex-core-voting:

MarteX Core wallet or masternode
------------------------------

If you started your masternode using the MarteX Core Wallet (not
recommended), you can vote manually from **Tools > Debug console**, or
directly from your masternode via SSH using ``martex-cli``. First look at
the proposal you want to vote on at either `MarteXCentral
<https://martexcoin.org/governance>`_ .You will see a command
for manual voting below the proposal description. Copy and paste the
command and modify it as necessary. As an example, take this proposal
from `MarteXCentral <https://martexcoin.org/governance>`_
The voting code for MarteX Core Wallet is as follows::

  gobject vote-many 18de3fb36b44098c83e4a3c18f398e8e6a97e00558a464bc0bc21dd6b3be0adf funding yes
  gobject vote-many 18de3fb36b44098c83e4a3c18f398e8e6a97e00558a464bc0bc21dd6b3be0adf funding no
  gobject vote-many 18de3fb36b44098c83e4a3c18f398e8e6a97e00558a464bc0bc21dd6b3be0adf funding abstain

Note that to vote from your masternode directly, you need to prefix the
command with ``martex-cli``, which is usually found in the ``.martexcore``
folder. The command should be similar to the following::

  ~/.martexcore/martex-cli gobject vote-many 18de3fb36b44098c83e4a3c18f398e8e6a97e00558a464bc0bc21dd6b3be0adf funding yes
  ~/.martexcore/martex-cli gobject vote-many 18de3fb36b44098c83e4a3c18f398e8e6a97e00558a464bc0bc21dd6b3be0adf funding no
  ~/.martexcore/martex-cli gobject vote-many 18de3fb36b44098c83e4a3c18f398e8e6a97e00558a464bc0bc21dd6b3be0adf funding abstain

Note this command will trigger a vote from all masternodes configured in
``MarteX.conf``. If you have multiple masternodes each with its own .conf
file, or if you want to vote with only some of your masternodes, you
must change the command from ``vote-many`` to ``vote``. If your vote was
successful, you should see a confirmation message reading **Voted
successfully**.

.. figure:: images/vote-martexcore.png
   :width: 300px

   Voting from the debug console in MarteX Core Wallet

You can also view a list of proposals in JSON format from the console to
copy and paste the proposal hash for voting as follows::

  gobject list

