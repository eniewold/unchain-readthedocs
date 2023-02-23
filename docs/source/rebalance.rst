######################
Re-balancing
######################

This functionality is used to create virtual transaction based on the difference between reported asset balance by an Exchange (or Wallet) and the unchain.app platform.

When the total of all transactions for a certain asset is different from the asset total reported by an Exchange or Wallet API; a transaction is created as type 'rebalance' and the amount is set to the delta between the two. 

We have enabled this functionality only for a limited amount of :doc:`exchanges` and :doc:`blockchain`.

For applicable connections, the re-balance function will be execute automatically at the appropiate moment, at the end of the synchronization. 

Transaction with type 'rebalance' can be deleted; although it will be created again when a next synchronization is started. 

When the re-balance function is used the first time a synchronization is done, the timestamp of the 'rebalance' will be near the first transaction that was synchronized. Otherwise the timestamp of the transaction will be set near the last synchronization transaction.