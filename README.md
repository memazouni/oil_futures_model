# Futures trade selection model
*Rank Seasonal Oil Trades and Backtest Profit/Loss*

***
###### ***Copyright © Justin Mackie. All Rights Reserved.  No one may distribute or create derivative works from my work without my written permission.  You are prohibited from using my code for commercial and/or business purposes.  However, you are permitted to fork and run my code solely for educational purposes on your personal (non-business) computer.***
***
#### <ins>Background:</ins>
Oil futures prices are time series data.  Each business day, there is one settlement price for the commodity.  The commodity illustrated in the model is Brent Crude, the key global price benchmark for Atlantic basin crude.  [Brent]( https://www.theice.com/products/219/Brent-Crude-Futures/specs)  is used to price the majority of Earth's internationally-traded crude supplies.

#### <ins>The Model:</ins>
My statistical seasonality model selects the best trades using historical data.  Then, cumulative trade Profit/Loss performance is tallied for the designated time period.  Model logic is built on Python and Pandas.  The Model reads and writes data from a SQLite3 database.  Data visualizations are plotted with Seaborn and Matplotlib.

We can run the model on a different commodity like West Texas Intermediate (WTI) or RBOB Gasoline Futures.  We just need appropriate data in a SQLite database!


#### <ins>Terminology:</ins>
* **Fit Years** - Years used in computing trade ranking stats.
* **Initial Price** - Price on Day before first day of month.
* **Last Price** - Last Price for day.
* **Roll Day** - Last day position is held.  For example, this may be a few days in advance of the expiration date.
* **Capital** - Position profit/loss.
* **Long Spread** - long front contract, short back contract.
* **Short Spread** - Short front contract, long back contract.
* **Front month** - first month in a spread.  Ex. 1 in a 1v3 spread.
* **Back month** - last  month in a spread.  Ex. 3 in a 1v3 spread.

* **Settles table** - settle - Daily settlement price of product

* **Spreads table** - spread - Settlement price difference for two different valid Contact Months on the same date.

* **Expiry table** - last_trade_date - the last day the Contract Month (prompt_month) is available.  Ex. BRENT future for May-2019  expired 03-29-2019.
