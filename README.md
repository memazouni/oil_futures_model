# Futures trade selection model
*Rank Seasonal Oil Trades and Backtest Profit/Loss*

***
###### ***Copyright © Justin Mackie. All Rights Reserved.  No one may distribute or create derivative works from my work without my written permission.  You are prohibited from using my code for commercial and/or business purposes.  However, you are permitted to fork and run my code solely for educational purposes on your personal (non-business) computer.***
***
#### <ins>Background:</ins>
Oil futures prices are time series data.  Each business day, there is one settlement price for the commodity.  The commodity illustrated in the model is Brent Crude, the key global price benchmark for Atlantic basin crude.  [Brent]( https://www.theice.com/products/219/Brent-Crude-Futures/specs)  is used to price the majority of Earth's internationally-traded crude supplies.

We can run the model on a different commodity like West Texas Intermediate (WTI) or RBOB Gasoline Futures.  We just need the data in a SQLite database!

#### <ins>The Model:</ins>
My statistical seasonality model selects the best trades using historical data.  Trade Profit/Loss performance is tallied for the adjacent period.  Model logic is built using Python and Pandas.  Model reads and writes data from a SQLite3 database.  Model data visualizations use Seaborn and Matplotlib.
