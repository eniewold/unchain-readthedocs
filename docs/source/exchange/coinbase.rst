######################
Coinbase
######################

.. note::

   This paragraph is about the Coinbase web application and mobile application and the 'Advanced Trading' interface of Coinbase. 

.. note::

   Also note that there are two methods of authentication using API keys; both are supported. Since the legacy method is deprecated, the instruction are updated for the latest method of API key generation.

Make sure to create a new connection in the unchain.app first as instructed, then follow these steps:

-----------------------
Standard
-----------------------
The following steps can be followed if you have the default Coinbase interface, and not enabled the Advanced view using the switch in the lower bottom of your Coinbase web application. 

* Login to Coinbase as usual. (make sure to use the official Coinbase site, not Coinbase Pro)
* Click on the user icon in the upper right corner to display a dropdown menu
* Select 'Settings' from the dropdown menu.
* After the settings page has loaded, select the 'API' tab
* Use the 'New API Key' button and enter your 2FA code
* Enter a name for the API key, for example: unchainapp (no dots allowed)
* Select the wallet the API key is applicable for using the dropdown list and select 'Default' or 'Standard' when only one available.
* Only select the 'View (read-only)' check-box for permissions
* Leave the IP white-list entry empty
* Click the 'Create and Download' button to generate the key
* Copy the 'API Key name' that starts with 'organization/' (using copy button in interface) string into the 'Key' property field (on unchain.app)
* Copy the 'API Secret' character string into the 'Secret' property field (on unchain.app). This is a long string; everthing should be pasted into the 'Secret' field on unchain.app.
* Test the entered keys using the 'Test API Keys' button in the unchain.app Connection dialog before saving
* Save the connection using the 'Save' button in the unchain.app Connection dialog.

-----------------------
Advanced
-----------------------
When using the Advanced view of the Coinbase web interface, click on the 'API' button on the left to access key creation. 