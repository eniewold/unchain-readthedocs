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


==========================
CSV File Import
==========================

For those Binance customers that no longer have access to the full user interface to create an API key due to local regulations and restrictions; you are able to export transactions through the limited interface of Binance after login.

* Login to Binance as usual (If you are restricted, you are redirected to a dialog with limited options)
* Hover over the export icon (next to the search box)
* Select 'Export Transaction Records' from the drop-down menu
* Select 'Customized' from the 'Time' drop-down
* Select a period (date range) to export
* Click Export button to queue the export
* Repeat the last steps for each year of data that needs to be exported
* Wait until you received an e-mail that download(s) is ready
* Then download the files by using the 'Download' link in last column of the submissions table
* Unpack the downloaded zip files first, before uploading them into unchain.app

.. note::
   We have noticed that the exported CSV files do not conver all types of transactions. This means that the results might have some currencies with negative values.
