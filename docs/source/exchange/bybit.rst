######################
Bybit
######################

Please following the following steps to generate API keys on the Bybit exchange and paste them into the unchain.app dialog:

* Login to Bybit as usual
* Make sure you have 2FA enabled, without it you can't create an API key
* Select your user icon in the top corner to show the drop-down menu
* Select 'API' from the drop-down menu
* Click the 'Create New Key' button and enter the fields as followed:
* API key usage: API transaction
* Name for API key: unchain.app (or to your liking)
* API Key Permissions: Read-Only and No IP restriction
* Types: 'Account Transfer' and 'Trade' (only)
* Click 'Submit' button and provide 2FA code
* Copy the shown 'API Key' character string into the 'Key' property field (on unchain.app)
* Copy the shown 'API Secret' character string into the 'Secret' property field (on unchain.app)

.. note::

   The exchange only communicates history up to 2 years old. Older transactions are currently not available through the API of the exchange.
