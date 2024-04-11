######################
Coinbase Pro
######################

.. note::

   For Coinbase (Web App and Mobile App) please see previous paragraph. This paragraph is about the Coinbase Pro Exchange (also known as GDAX) only. 
   Since the release of 'Advanced Trading', not all accounts can access the Coinbase Pro interface anymore. You can still generate an API key to synchronize all trades made prior to migration to 'Advanced Trading'.

The following steps will allow you to create an API key for communication with unchain.app through the Coinbase Pro web application. 

* Login to Coinbase Pro as usual. (make sure to use the official Coinbase Pro Exchange site, not the Coinbase App)
* Click on the user icon in the upper right corner to display a dropdown menu
* Select 'API' from the dropdown menu.
* Use the 'New API Key' button and a pop-up dialog will appear
* Enter a nickname (for example "unchain") in the 'API key nickname' field
* Make sure the 'View' check-box is checked (only)
* Copy the shown 'Passphrase' into the 'Phrose' property field (on unchain.app)
* Leave the 'IP Whitelist' field empty
* Click the 'Create API Key' button
* Enter 2FA code when aske
* Copy the 'API Secret' character string into the 'Secret' property field (on unchain.app)
* Close the dialog with the secret and find the generated API entry in the overview.
* Copy the character string above the 'Nickname' into the 'Key' property field (on unchain.app)
