######################
BitMEX
######################

Please following the following steps to generate API keys on the BitMEX exchange and paste them into the unchain.app dialog:

* Login to BitMEX as usual.
* Hover over the circle with your initial to show the drop-down menu.
* Select 'API Keys' from the drop-down menu.
* Under the 'Create an API Key' enter a name (for example unchain.app)
* Leave CIDR unchanged (IP address whitelisting is not supported yet)
* Leave 'Key Permissions' to hyphen ('-') for read only access
* Leave 'Withdraw' unchecked for maximum security
* Enter your 2FA code if applicable
* Click on the 'Create API Key' button
* Copy the shown 'ID' character string into the 'Key' property field (on unchain.app)
* Copy the 'Secret' character string into the 'Secret' property field (on unchain.app)

-------------------------
Comments
-------------------------

* There is a limit of 1000 transactions, contact us if you encounter this maximum!
* Only transactions denoted with type 'Withdrawal', 'RealisedPNL', 'Deposit' and 'Transfer' are processed.
* Only transactions with status 'Completed' are processed to avoid processing transactions that might become cancelled.
