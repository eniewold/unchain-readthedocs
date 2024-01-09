######################
Connections
######################

These pages explain how to set up a connection to a wallet or exchange. Connection properties are used by the system to connect to schedule synchronization and connect to wallets and exchanges.

======================
Manage Connections
======================

You can manage connections through the 'Connections' page, available through the side menu. The page will show all previously created connections in a table.
The table shows per connection a number of details, like: Name, Description, Status and last update timestamps. By selecting a row of the table, the connection properties can be altered, and you will have access to additional actions that can be executed for that connection.

The page includes a button to add a new New Connection. A list of all supported connection sources will be displayed (both Exchanges and Blockchain wallets). To actually create a new connection, choose the wanted source and fill the requested properties in the dialog. Depending on the type of source, different properties can be entered. 

==============================
Exchange Connection Properties
==============================

The properties of an exchange connection are used by the system to retrieve transaction details. Exchanges offer an API (Application Programmers Interface) that can be used to retrieve information. Most exchanges require a number of private details to shared with our application before the synchronization can start. Our system will automatically enable/disable the required fields.

.. note::
   Some properties are considered sensitive data; these are only shown when the connection is created and are hidden when the connection properties are altered.

The following properties are available for an Exchange Connection:

* **Exchange** - The actual exchange to connect (selectable when new connection is created)
* **Name** - Name you wish to give this connection
* **Key** - API key (see :doc:`exchanges` for more details)
* **Phrase** - API phrase (if applicable, see :doc:`exchanges` for more details)
* **Secret** - API secret (see :doc:`exchanges` for more details)
* **Ignored** - The connection will be ignored by the system (no synchronization and invisible in portfolio)
* **Paused** - The synchronization will not start when scheduled. All transaction data is available normally.

Check the :doc:`exchanges` documentation for more details per supported exchange.

============================
Wallet Connection Properties
============================

A wallet connection is used to retrieve details from a certain blockchain. Each wallet connection has a number of properties that are used by the system to synchronize transactions. 

.. only:: html

   .. image:: images/wallet_connection_dialog.png
      :width: 400
   
The following properties are available for an Exchange Connection:

* **Blockchain** - The actual blockchain where the wallet address references to (selectable when new connection is created)
* **Name** - Name you wish to give this connection
* **Active** - The connection will be made unavailable by the system (no synchronization and invisible in portfolio)
* **Paused** - The synchronization will not start when scheduled. All transaction data is available normally.

---------------------------
Wallet Connection Addresses
---------------------------

You can add addresses to monitor and synchronize by using the available buttons. 

* **Add Address** button: Add a single address manually (we recommend using copy/paste)
* **from Ledger USB** button (for blockchains that are supported by the Ledger USB hardware key): The dialog will allow you to retrieve a number of different addresses using your connected USB hardware key.
* **from Web3 Wallet** (for supported blockchains): When you have an active Web3 Wallet extension in your browser, this will allow you to retrieve the active account addresses from that wallet. 

.. note::
   The address format is checked for a number of blockchains, but you should always make sure you use the correct address to avoid confusing synchronization results.

Check the :doc:`blockchains` documentation for more details per supported blockchain.

.. _connections_manual:
========================
Manual Ledger Connection
========================

A manual ledger connection allows you to manually add new transactions (effectively a ledger. NB. not related to the usb hardware key). Useful for transactions that are moved out of sight, like staking. 

For manual transactions and mirrored transactions, you will need to have at least one manual ledger connection added. 

.. _connections_status_model:
=======================
Connection Status Model
=======================

There are a number of different states a connection can be in. The following items explain the possible states:

* **Standby** - Waiting for next background synchronization. The Queue Time column shows the expected time.
* **Queued** - Background synchronization is about to start, the task is waiting to be picked up by our systems.
* **Syncing** - Background sync is being performed, please be patient while we are working on this (no need to keep the application open). Notifications will be created for new transactions. Transactions are visible after synchronization is finished. Some connection types support progress monitoring.
* **Error** - Some occurred during sync, check :doc:`notifications` for the reason. You might need to correct the properties and unpause the connection.
* **Untested** - New or changed connection. The system will automatically validate the entered details with the Exchange. Once tested, synchronization will continue.
* **Paused** - Paused (perhaps due to error); uncheck to make available for synchronization.
* **Inactive** - There was no activity detected within the subscriptions 'Inactivity Period', connection is also Paused. Unpause to restart synchronization.
* **Suspended** - The referenced blockchain or exchange is no longer operational. This status is automatically applied by the system. Synchronization is no longer available. Already synchronized transaction are kept available.
* **Ignored** - Connection is ignored by the system.

It is possible two states are active at the same time; for example 'paused' and 'error'.

======================
Re-balancing
======================

Re-balancing is activated for a number of different Exchanges and Blockchains. Most of the times this is done due to the fact that the offered API does not offer a complete set of transactions.

The re-balance functionality will calculate any differences per Asset between Exchange/Wallet and unchain.app totals and create transactions with delta value per asset to counter the difference. The transaction type is set to 're-balance' to differentiate these transactions. Note that these transactions can be deleted, since they don't represent an actual transaction on the Exchange or Blockchain.

The re-balance function is activated automatically and is executed after a Exchange or Wallet synchronization. 

======================
Jump Queue
======================

Synchronization of a connection is scheduled automatically. The frequency of synchronization is based on the active subscription. But all users can use the 'Jump Queue' function to synchronize the selected connection as soon as possible.

When this function is initiated by a user, the maximum number of times this function can be used is decreased. Check :doc:`subscriptions` for more details. There are system events that also trigger this function, those will note be counted towards the maximum usage. 
