######################
Re-balancing
######################

This functionality is used to create (virtual) transaction based on the difference between reported asset balance by an Exchange (or Wallet) and the unchain.app platform.

When the total (on unchain.app) of all transactions for a certain asset is different from the asset total reported by an Exchange or Wallet API; a transaction is created as type 'rebalance' where the amount is set to the delta between the two. 

We have enabled this functionality only for a limited amount of :doc:`exchanges` and :doc:`blockchains`.

For applicable connections, the re-balance function will be execute automatically at the end of the synchronization. 

Transaction with type 'rebalance' can be deleted; although a fresh rebalance transaction will be created again after a next synchronization is started. 

When the re-balance function is used the first time a synchronization is done, the timestamp of the 'rebalance' will be near the first transaction that was synchronized. Otherwise the timestamp of the transaction will be set near the last synchronization transaction.

Why?
---------------------

Since not all exchanges give access to all transaction data, sometimes the actual balance can't be derived from the total of all transactions. 
For example; Some exchange have a time limit they store your transactions, other don't have an actual API for a complete set of transactions.
The same counts for Blockchain Wallets; not all our wallet detail providers have a (timely) matter of reporting all types of transaction; although for blockchain wallets this is not very common.