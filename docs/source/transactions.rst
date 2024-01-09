######################
Transactions
######################

This page will allow you to browse through all synchronized transaction from both Exchanges and Blockchain Wallets. The page is accessible through the 'Transactions' page link in the menu. This documentation page will explain the data shown and how to filter/search through the data.

.. note::
   Transactions on this page area always limited to the selected year. Make sure you double check the year drop-down for the requested data.

======================
Calendar Heat-map
======================

The top part of the page contains a calendar view of a complete year (the year as selected). Each cell represents a day and is colored based on the number of Transactions on that day in contrast to other days of the year. Relative high amounts of Transactions are colored from yellow to red. Days without Transactions are white.

.. only:: html
   .. image:: images/transactions_heatmap.png

You can click on any day of the calendar to move the table view to that particular day. The table page and scroll position are changed, this might not be 100% accurate. 

======================
Transactions Table
======================

Below the heat-map you can find a table with all transaction details for selected :ref:`transactions_filters`. The following columns are included in the table:

* **Timestamp** - The actual timestamp (in seconds) as communicated by exchange or blockchain, displayed in your local timezone. 
* **Connection** - Exchange or Wallet connection this transaction belongs to.
* **Account** - If applicable; account name as used by a Exchange. *deprecated*
* **Type** - Type of transaction as determined by our system. See :ref:`transactions_types` for more details.
* **Description** - Text as received during synchronization. User editable notes will be displayed as a small icon that can be hovered for details.
* **Amount** - Amount of assets for this transaction. Negative is outgoing, positive is incoming. 
* **Currency** - Currency symbol for the asset amount.
* **Value (then)** - Value in your selected fiat currency at time of synchronization. Estimated value are prefixed by ≈ symbol and colored lighter. Other values are exact amounts (and are mostly communicated by the exchange).
* **Trading Pair** - If the transaction involves a trade, this column displays the symbol of the traded currency pair (normalized by our system, exchange symbol might differ).

You can click on a row to display the Transaction Details dialog which includes some additional details.

.. note::
   The amount of space in your browser determines the columns shown. There might be columns hidden automatically. You can increase resolution or window size or zoom out (CTRL -/+) to allow more space for columns.

There are several buttons with the following functionality:

* **Add** - This will allow you to add a new (manual ledger) transaction. First make sure you add a :ref:`connections_manual`. An empty transaction dialog is shown that can be used to enter the transaction properties. 
* **Export** - See section :ref:`transactions_export`.
* **Reload** - When new transactions have been synchronized, or a synchronization has been restarted manually, you can force a reload of all transactions. 

.. _transactions_filters:
----------------------
Filters
----------------------

The displayed transactions in the table can be filtered using the following controls, displayed above the table:

.. only:: html
   .. image:: images/transactions_filters.png

* **Filter** - Free text to search for.
* **Year** - Only show transactions with timestamp in selected year.
* **Currency** - Only show transactions with selected currency asset.

.. _transactions_export:
----------------------
Export
----------------------

The displayed transactions can be exported to a number of different format using the 'Export' button:

* **CSV** - Comma Separated Values, a (fairly) standard way of exporting data in rows and columns that can be imported by a number of applications. 
* **Excel** - File that is formatted for direct usage in Excel, with date and numbers correctly formatted for international usage. 
* **Print** - Report with a limited number of columns. Data is only filtered using keyword and currency. 
  
.. _transactions_types:
======================
Transactions Types
======================

There are a number of different transaction types, usage is documented below:

* **deposit** - Received amount into wallet or exchange.
* **withdraw** - Transmitted amount out of wallet or exchange.
* **sell** - Traded (or swapped) amount from given currency.
* **buy** - Traded (or swapped) amount into given currency.
* **fees** - Cost of transaction or trade.
* **interest** - Rewards, usually for staking or earning.
* **cashback** - Reward, other than interest.
* **reward** - Also used to denote rewards.
* **rebalance** - Result of :ref:`rebalance` action.
* **input** - On-ramp (usually fiat) deposit - only manually selectable.
* **output** - Off-ramp (usually fiat) withdrawal - only manually selectable.
* **unknown** - Type could not be recognized.
* **airdrop** - Amount automatically received from 3rd party.

You can alter the transaction type of any transaction using the :ref:`transactions_dialog`. Use the 'Change Type' drop-down button to alter the type. Only types with the same direction (incoming or outgoing) can be selected. 

.. only:: html
    .. image:: images/transaction_changetype.gif

If the altered transaction type is not correct, you can always revert back to the originally synchronized type by selecting the 'Revert back to original type' option in the drop-down. 

.. _transactions_dialog:
======================
Transactions Dialog
======================

When a row in the transactions table is clicked, the 'Transaction details' dialog is shown. There are three tabs 'Properties', 'Related' and 'Details' with the following fields:

* **Connection** - Exchange or Wallet connection this transaction belongs to.
* **Timestamp** - The actual timestamp (in seconds) as communicated by exchange or blockchain, displayed in your local timezone. 
* **Account** - If applicable; account name as used by a Exchange. *deprecated*
* **Type** - Type of transaction as determined by our system. See below for more details.
* **Address From** - (if available) A wallet address the transaction was received from.
* **Address To** - (if available) A wallet address the amount was transmitted to.
* **Description** - Text as received during synchronization.
* **Amount** - Amount and assets for this transaction. Negative is outgoing, positive is incoming. 
* **Value (then)** - Value in your selected fiat currency at time of synchronization. Estimated value are shown as '(approx)', other values are exact amounts (and are mostly communicated by the exchange).
* **User Notes** - Free text for you to add to a transaction. When added, a small icon is shown next to the description cell.
* **Foreign ID** - Unique string used by the wallet or exchange to identify the transaction. 
* **Context** - A technical field that can contain details as communicated by the exchange or blockchain provider. Not always used. 

The **Related** tab wil show a table with transactions that are related. This relation is determined during synchronization and usually involves a trade and/or fees. 