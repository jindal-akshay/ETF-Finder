# Fund Finder



## Sites used for webscraping:
Closing price of stock: https://finance.yahoo.com/quote/

ETF ranking database:https://etfdb.com/etf


## Background

As early investors start putting money into savings accounts (401k, RothIRA), these individuals might be interested in knowing how many shares they own of a particular stock of interest. 

The process involved:

1. [User Submission](#User-Requirements) 
2. [Webscraping](#Webscraping)
3. [Calculations](#Calculations)
4. [Forward Thinking](#Next-Steps)


### User Requirements

The user is asked three simple questions to answer to determine the amount of shares owned of a particular stock within the multiple ETF's. 

1. What stock are you interested in:
2. What ETF's are you invested in (Need 5 entries):
3. What is the dollar amount invested in each ETF:


### Webscraping 

Queries were sent to ETFDB for each ETF the user has entered. The query will parse through the page to extract the 'top 15 stock holdings' table. 

To obtain the closing price of the stock of interest, queries made to Yahoo Finance to obtain the "previous close" value.

### Calculations

Concat all succesful searches in of the stock within the requested ETFs into a single DataFrame. To obtain the dollar amount owened for each stock within the ETF, we are given the holding allocation and the dollar amounts invested in ETF. Therefore, used those two variables to find out the dollar allocation for each holding within the ETF.

The final share amount calculation, it utilizes the sum of dollar allocations to the stock of interest, divided by the closing price of the stock.


### Next Steps

1. Utilize AmazonLex for a better UI
2. reduce the DRY for calculations
3. Create different statistics such as details about holdings