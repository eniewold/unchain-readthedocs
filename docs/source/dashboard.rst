######################
Dashboard
######################

The dashboard page shows a number of key performance indicators and frequently accessed data for quick reference and monitoring of your cryptocurrency portfolio.

It's also a starting point for configuration and further analysis of data. Below are the sections documented. 

.. note::
   Some columns of data are hidden when there is not enough room on the screen. You can increase the window size or zoom out to reveal them. 

======================
Portfolio
======================

This table shows for each of your assets the symbol, amount and current value. You can click on any asset to open the :doc:`assets` page for details on that asset. The table is sorted by current value (descending). 

Use the button 'Portfolio' in the top corner to open the :doc:`portfolio` page. 

======================
Connections
======================

This table shows the name, number of transactions and current value of all your wallet and exchange connections. You can select any line to go to the :doc:`connections` page for the connection properties. The table is sorted by current value (descending). 

Use the button 'Connect' in the top corner to open the :doc:`connections` page, to create new connections.

======================
Transactions
======================

This table shows the newest 100 transactions that were synchronized for all selected connections. The table shows the timestamp, type, connection, amount and currency for each transaction. 

Use the button 'Transactions' in the top corner to open the :doc:`transaction` page to view browse through the complete set of transactions.

======================
Asset Value
======================

This tab shows a donut chart with slices by asset value. Asset values smaller than 1% are combined into a single donut chart slice. Hover mouse over the chart to reveal additional details. 

Next to the chart the following asset (fiat) values are shown:
* Current total value
* Asset value change since beginning of week
* Asset value change since beginning of month
* Asset value change since beginning of year

.. note::
   Like most values in the application, these values will also change when the :doc:`backintime` function is used. So double check if that function is activated.

======================
Distribution
======================

This donut chart shows the total asset fiat value per connection. Hover mouse over the chart to reveal additional details. 

======================
Value History
======================

This charts plots a line based on the historic fiat value of your assets, one point per day in the past. Each point represents the total asset value at the close of that day. Hover mouse over the chart to reveal additional details. 

.. note::
    Calculation of this history might take some time if you have a large number of transactions, and the chart is viewed for the first time.
