.. meta::
   :description: Maintaining a MarteX masternode involves staying up to date with the latest version, voting and handling payments
   :keywords: martex, cryptocurrency, masternode, maintenance, maintain, payments, withdrawal, voting, monitoring, upgrade, deterministic

.. _masternode-maintenance:

===========
Maintenance
===========

Masternodes require regular maintenance to ensure you do not drop off
the payment queue. This includes promptly installing updates to MarteX, as
well as maintaining the security and performance of the server. In
addition, masternodes should vote on proposals and perform other tasks
in the interest of the network and the value of the MarteX they hold.


.. _masternode-update:

Masternode Software Update
==========================

The MarteX Core software requires regular updates in order to remain
consistent with the current network consensus. Depending on whether you
installed MarteX manually or using mxt-mn, you must follow the procedure
appropriate for your masternode, as described below.


Option 1: Updating from mxt-mn
------------------------------

To update MarteX using mxt-mn, see this `link <https://github.com/martexcoin/mxt-mn>`_.


Option 2: Manual update
-----------------------

To update MarteX manually, log in to your server using ssh or PuTTY. If
your crontab contains an entry to automatically restart martexd, invoke
``crontab -e`` and comment out the appropriate line by adding the ``#``
character. It should look something like this::

  # * * * * * pidof martexd || ~/.martexcore/martexd

Then stop MarteX running::

  ~/.martexcore/martex-cli stop

Visit the `GitHub releases page
<https://github.com/martexcoin/martexcoin/releases>`_ and copy the link to the
latest x86_64-linux-gnu version. Go back to your terminal window and
enter the following command, pasting in the address to the latest
version of MarteX Core by right clicking or pressing **Ctrl + V**::

  cd /tmp
  wget https://github.com/martexcoin/martexcoin/releases/download/v4.0.2.2-fix/martexcore-4.0.2-x86_64-linux-gnu.tar.gz

Verify the integrity of your download by running the following command
and comparing the output against the value for the file as shown in the
``SHA256SUMS.asc`` file::

  sha256sum martexcore-4.0.2-x86_64-linux-gnu.tar.gz

Extract the compressed archive and copy the new files to the directory::

  tar xfv martexcore-4.0.2-x86_64-linux-gnu.tar.gz
  cp -f martexcore/bin/martexd ~/.martexcore/
  cp -f martexcore/bin/martex-cli ~/.martexcore/

Restart MarteX::

  ~/.martexcore/martexd

You will see a message reading "MarteX Core server starting". We will now
update Sentinel::

  cd ~/.martexcore/sentinel/
  git checkout master
  git pull

Finally, uncomment the line to automatically restart MarteX in your
crontab by invoking ``crontab -e`` again and deleting the ``#``
character.

The MarteX software on the masternode is now updated.


Proof of Service Bans
=====================

If your masternode fails to provide service to the network in accordance
with the current consensus rules, it will receive a :ref:`Proof of Service Ban <proof-of-service>`.
If your masternode is in the ``POSE_BANNED`` status, you should check
the following settings are configured correctly:

- Ensure you are running the :ref:`latest version of MarteX <masternode-update>`
- Ensure your masternode has sufficient memory, swap, processing power 
  and hard drive space
- Ensure you are fully synced to the `correct blockheight <https://be.martexcoin.org>`_, 
  and that you are on the correct chain and not forked off
- Ensure that marternode private key is specified using the 
  ``masternodeprivkey`` option in the masternode's ``MarteX.conf`` file
- Ensure that the masternode private key on the masternode is unique on the 
  network and not shared with any other masternodes
- Ensure that the ``externalip`` (and ``port`` if using testnet) are 
  specified correctly and not blocked by a firewall or port forwarding 
  service
- Ensure that Sentinel is installed, updated, not exiting with an error 
  and is entered in your crontab to run every * * * * * `time <https://github.com/martexcoin/sentinel#set-up-cron>`_.

Once you are certain these settings are correct, you can update your
service status on the network. Monitor your
masternode closely using ``masternode status`` and/or the ``debug.log``
file after restoring service. This information can help you pinpoint the
specific misconfiguration that is causing the masternode to be banned.
The masternode will be banned again if it continues to fail to provide
service.


Masternode monitoring tools
===========================

Several sites operated by community members are available to monitor key
information and statistics relating to the masternode network.

Block Explorers
---------------

Since MarteX is a public blockchain, it is possible to use block explorers
to view the balances of any MarteX public address, as well as examine the
transactions entered in any given block. Each unique transaction is also
searchable by its txid. A number of block explorers are available for
the MarteX network.

- `MarteXcoin blocker explorer <https://be.martexcoin.org>`_ offers a block explorer
  with detailed visualizations to analyse the MarteX blockchain.
- `CoinCheckup <https://coincheckup.com/coins/martexcoin/>`_ offers a
  range of statistics and data on most blockchains, including MarteX.
