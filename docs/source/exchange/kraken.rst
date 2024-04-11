######################
Kraken
######################

Please following the following steps to generate API keys on the Kraken exchange and paste them into the unchain.app dialog:

* Login to Kraken as usual
* On the top corner, click your name for drop-down menu
* Select 'Security' for a sub-menu, and select 'API' menu entry
* Use the 'Add key' link in top of the pane
* Enter a description, for example 'unchain.app'
* Leave the 'Nonce window' value at 0
* Select Permissions: 'Query Funds', 'Query closed orders & trades', 'Query ledger entries' and 'Export Data' (for security, leave other unchecked!)
* Leave other fields empty
* Save using the 'Generate Key' button
* Enter 2FA details if requested/configured
* Copy the shown 'API Key' character string into the 'Key' property field (on unchain.app)
* Copy the 'Private Key' character string into the 'Secret' property field (on unchain.app)

.. note::

   Don't share the same API keys from Kraken with another application; since that might interfere with synchronization.

-------------------------
Comments
-------------------------

* Some currency assets have legacy symbols (like XBT); unchain.app will automatically translate this into the modern symbols to avoid confusion.
* Our system will automatically try to link related transactions (such as trades and fees), although this is not always match 100%.
* Subsequent synchronizations are sped up by saving the last synchronized transaction details. Please allow some additional time for the first (initial) synchronization.
