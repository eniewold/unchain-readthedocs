######################
Binance
######################

This page contain instruction on how to connect the unchain.app to the Binance exchange to retrieve transactions.

.. note::
   Binance does not support a complete set of transaction synchronization, but we've managed to support as much as possible on several different available API's that are offered by Binance. 
   To counteract any possible difference between Binance balances and total balance as calculated by unchain.app on all transaction, :doc:`rebalance` is supported. 

You can enter generated keys into the Exchange properties dialog after using the 'New Exchange Connection' button on the 'Connections' page. 

Please following the following steps to generate API keys on Binance and paste them into the unchain.app dialog:

* Login to Binance
* Hover over the account icon and select 'API Management' from the pop-up menu
* Use the 'Create API' button
* Select 'System generated' when requested and click Next
* Enter a label, for example 'unchain app' and click Next (no special characters allowed)
* If requested; solve the captcha puzzle
* If applicable/requested; generate e-mail verification code
* If applicable/requested; enter your 2FA authenticator code and click Next
* Copy the shown 'API key' character string into the 'Key' property field (on unchain.app)
* Select and copy the 'Secret Key' character string into the 'Secret' property field (on unchain.app)
* Make sure the 'API restrictions' are 'Enable reading' only for maximum security (default is probably correct)

--------------------------
Comments
--------------------------

* The Binance API does not allow a large number of requests per minute; synchronization will take longer when all trading pairs are synchronized. 
* Our synchronization component detects if no changes are available and will finish quickly.
* :doc:`rebalance` is active and executed at the end of the synchronization cycle to ensure correct asset balances.