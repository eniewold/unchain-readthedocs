######################
Crypto.com App
######################

The Crypto.com (mobile) App does not have a API interface for automatic synchronization. You can export CSV files with transactions from within the App itself. Please follow these instructions when in the Crypto.com App:

* Go to the 'Accounts' page
* Click upper right icon (timer with dollar icon) to enter 'Transaction History' page
* Click upper right icon again (box with arrow up icon) to access 'Export' and 'Export History' tabs
* Select 'Crypto Wallet' as transaction source
* Select a 'From' and 'To' date (maximum selection is a year, so repeat steps to export everything in multiple files)
* Click on the 'Export to CSV'
* Select 'Fiat Wallet' as transaction source and use 'Export to CSV'
* Repeat above steps for all years you want to export (this is only needed once)
* Go to the 'Export History' tab
* Click on 'Download' link next to each generated file (connect to WiFi is download does not work)
* Import all downloaded 'crypto_transactions_*.csv' and 'fiat_transactions_*.csv' files into unchain.app

.. note::

   You can have multiple (migrated) accounts at this exchange when you are using an older account. Make sure to synchronize (or export) your transactions before merging or removing older accounts. Since removing or merging might remove transaction history from the exchange itself.

   You will need to export all data (year by year) when you created the connection in unchain.app. After that you can select a date range that covers the new transactions. Overlap of data is no problem, duplicates are detected by our systems.
