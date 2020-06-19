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

*The Settings menu in Dash Android Wallet*

The settings menu contains a range of options to control the behavior of
the MarteX Android Wallet. To access the settings, tap the **Menu
button**, then **Settings**. You can then choose between **Settings**,
**Diagnostics** and **About**, which displays wallet version, copyright,
license and source code information.

Settings
^^^^^^^^

Denomination and precision
  Select the number of decimal places to show for DASH denominations, or
  switch to mDASH or µDASH denominations

Own name
  Enter a short name to be included in your QR codes when displaying to
  other users for scanning. The short name will then appear as a label
  in their wallet to verify the recipient and simplify address
  management.

Auto-close send coins dialog
  Specify whether or not to close the send dialog once a payment is 
  complete.

Connectivity indicator
  Enables display of an indicator in the Android notification area to be
  able to quickly verify connectivity.

Trusted peer
  Enter the IP address or hostname of a single peer to connect to.

Skip regular peer discovery
  Enabling this option prevents automatic peer discovery and forces 
  connection to the one specified trusted peer only.

Block explorer
  Allows you to select which block explorer you want to use for
  functions linking to a block explorer.

Data usage
  Links to the Android **Data usage** function to view and/or restrict
  data usage for the app.

Balance reminder
  Enables an Android system notification to remind you of any unspent
  Dash if you don't open the app in that time.

Enable InstantSend
  Enables functionality to use InstantSend to send and receive Dash.

Enable Lite Mode
  Enabling lite mode reduces bandwidth usage.

Show disclaimer
  Enables or disables various disclaimers and warning messages in the
  app.

BIP70 for scan-to-pay
  Enables use of the `BIP70 payment protocol
  <https://github.com/bitcoin/bips/blob/master/bip-0070.mediawiki>`_ to
  add further verification and security features when scanning QR codes.

Look up wallet names
  Enables use of `DNSSEC <https://en.wikipedia.org/wiki/Domain_Name_Syst
  em_Security_Extensions>`_ to attempt to identify a wallet name when
  creating transactions.

Diagnostics
^^^^^^^^^^^

Report issue
  Allows you to gather a range of information related to your wallet in
  order to send a bug report to developers for troubleshooting.

Show xpub
  Displays the extended public key for the seed used to generate
  addresses in your wallet. Providing your xpub to a third party will
  allow them to view your entire transaction history, but not make new
  transactions.

Reset block chain
  Resets data stored on your device relating to the blockchain. This
  data will need to be collected again from full nodes, similar to when
  setting up a new wallet. This process may take some time.
