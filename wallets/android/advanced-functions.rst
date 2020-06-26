.. meta::
   :description: Set up address book, exchange rates, sweep paper wallets and change settings in the MarteX Android wallet.
   :keywords: martex, mobile, wallet, android, address book, paper, exchange rates

.. _martex-android-advanced-functions:

Advanced functions
==================

Sweep paper wallet
------------------

Sweeping a paper wallet is a method of transferring the value stored on
an address you may have received as a paper wallet or from an ATM into
your own wallet. You must have access to the private key for an address
to use this function. In this process, all MarteX stored on the address
will be sent to a new address that has been deterministically generated
from your wallet seed. The private keys you sweep do not become a part
of your wallet.

To sweep a paper wallet, tap the **Menu button** and select **Sweep
paper wallet**. Tap the **Scan** button and scan the QR code from your
paper wallet. Once the private key has been identified, tap **Sweep** to
create the transaction moving the MarteX into your own wallet. Once this
transaction is confirmed, the paper is worthless and should be
destroyed.

.. image:: img/menu-sweep.png
   :width: 160 px
.. image:: img/sweep-start.png
   :width: 160 px
.. image:: img/sweep-scan.png
   :width: 160 px
.. image:: img/sweep-done.png
   :width: 160 px

*Sweeping a paper wallet with 0.10 MarteX into the Android Wallet*


Settings
--------

.. image:: img/menu-settings.png
   :width: 160 px
.. image:: img/settings.png
   :width: 160 px

*The Settings menu in MarteX Android Wallet*

The settings menu contains a range of options to control the behavior of
the MarteX Android Wallet. To access the settings, tap the **Three dots in the upper right corner**.
 You can then choose between **Currency Swap Rates**,
**Transaction fee**, **Show recovery phrase**, **Restore your wallet**,
 **Manual receiving address** and **Depuration**.

Currency Swap Rates
^^^^^^^^^^^^^^^^^^^

Displays how much MarteXcoin is worth in each F.IA.T money.

Transaction fee
^^^^^^^^^^^^^^^

Displays the minimum transaction fee for the currency.

Show recovery phrase
^^^^^^^^^^^^^^^^^^^^

Show recovery phrase

Restore your wallet
^^^^^^^^^^^^^^^^^^^

Initiates the process of restoring your wallet or creating a new one.

Manual receiving address
^^^^^^^^^^^^^^^^^^^^^^^^

Prevents the wallet from automatically creating new addresses with each transaction carried out.

Depuration
^^^^^^^^^^

You can use a collection of tools to debug various problems with your wallet.
  Portfolio unlocking tests.
