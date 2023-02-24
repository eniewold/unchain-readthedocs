######################
Blockchains
######################

These pages contain details on configuring a new Blockchain Wallet Connection. Creating new connections is only available in the web application. 

****************************
Create new Wallet Connection
****************************

Go to the 'Connections' page and use the 'New Wallet Connection' button to display the blockchain selection dialog. Select the blockchain you have a wallet address for and want to synchronize. 

In the properties dialog, make sure to enter an appropriate name for the wallet. Including the blockchain name itself can be helpful if you have different wallets for same blockchain.  

Make sure to copy/paste your wallet address from the wallet application (like Metamask or Ledger) to make sure the correct wallet is monitored. Use the 'Multiple Addresses' button to enter a list of addresses to monitor, one address per line. 

Note that there is (some) address format verification active, which is checked when you save the entered data. 

The 'Ignored' property will make all related transaction data unavailable to the system. 

The 'Paused' property can be set if synchronization is no longer needed or wanted. This property can also be set by the system when problems during synchronization occur.

.. note::
   First time synchronization might take a while, please be patient. Subsequent synchronization is much faster. 

****************************
Supported Blockchains
****************************

Blockchains as listed below are supported. As much transaction details as (currently) possible are synchronized periodically and automatically. 

Please refer to the sections below for notes on synchronization limitations per blockchain.

======================
Ethereum
======================

You can also use the 'Ledger Nano USB' button to connect you Ledger hardware wallet and retrieve addresses automatically. 

* :doc:`realtime` transaction detection supported
* Native (ETH) and ERC20 tokens are supported
* When a (new or unsalable) token does not appear; please contact :doc:`support` with the expected token details.

======================
Bitcoin
======================

* :doc:`realtime` transaction detection supported
* Only native currency supported (BTC)

======================
Binance Smart Chain
======================

* Native (BNB) and tokens are supported
* When a (new or unsalable) token does not appear; please contact :doc:`support` with the expected token details.

======================
Litecoin
======================

* Only native currency supported (LTC)

======================
eCash
======================

* Only native currency supported (XEC)

======================
Dash
======================

* Only native currency supported (DASH)

======================
ZCash
======================

* Only native currency supported (ZEC)

======================
Dogecoin
======================

* Only native currency supported (DOGE)

======================
Groestlcoin
======================

* Only native currency supported (GRS)

======================
Bitcoin Cash
======================

* Only native currency supported (BCH)

======================
Cronos
======================

* Native (CRO) and tokens are supported
* When a (new or unsalable) token does not appear; please contact :doc:`support` with the expected token details.
* Same currency, but different blockchain as Crypto.org

======================
Crypto.org
======================

* Native (CRO) and tokens are supported
* When a (new or unsalable) token does not appear; please contact :doc:`support` with the expected token details.
* Same currency, but different blockchain as Cronos

======================
Terra 2.0
======================

* Native (LUNA) and tokens are supported
* When a (new or unsalable) token does not appear; please contact :doc:`support` with the expected token details.
* Replacement blockchain for Terra Classic

======================
Terra Classic
======================

* Native (LUNC) and tokens are supported
* When a (new or unsalable) token does not appear; please contact :doc:`support` with the expected token details.
* Replaced by Terra 2.0 blockchain
