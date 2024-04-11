######################
Coinbase
######################

.. note::

   This paragraph is about the Coinbase web application and mobile application and the 'Advanced Trading' interface of Coinbase. For (partially deprecated) Coinbase Pro (Exchange formerly known as GDAX), please see next paragraph. 

The following steps will allow you to create an API key for communication with unchain.app through the Coinbase web application. 

* Login to Coinbase as usual. (make sure to use the official Coinbase site, not Coinbase Pro)
* Click on the user icon in the upper right corner to display a dropdown menu
* Select 'Settings' from the dropdown menu.
* After the settings page has loaded, select the 'API' tab
* Use the 'New API Key' button and enter your 2FA code
* Under the 'Accounts' header in the pop-up dialog, check the 'All wallets' box
* Under the 'Permissions' header, check the following permissions: 'wallet:accounts:read', 'wallet:deposits:read', 'wallet:trades:read', 'wallet:addresses:read', 'wallet:orders:read', 'wallet:transactions:read', 'wallet:withdrawals:read'
* Leave 'Notifications' and 'Security Settings' section unchanged
* Click the 'Create' button to generate keys
* Copy the shown 'API Key' character string into the 'Key' property field (on unchain.app)
* Copy the 'API Secret' character string into the 'Secret' property field (on unchain.app)
