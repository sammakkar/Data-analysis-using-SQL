# Data-analysis-using-SQL
Executed various SQL queries on NFT data to get data driven insights.

# NFT Sales Analysis Using SQL

## Overview
This project focuses on analyzing Cryptopunks NFT sales data recorded on the blockchain from January 1, 2018, to December 31, 2021. The dataset contains detailed information such as buyer and seller addresses, transaction details, NFT IDs, ETH prices, and USD prices. Using SQL, we uncover market trends, identify high-value sales, and compute key statistics for informed decision-making in the evolving NFT space.

## Queries performed
1. How many sales occurred during this time period? 
2. Return the top 5 most expensive transactions (by USD price) for this data set. Return the name, ETH price, and USD price, as well as the date.
3. Return a table with a row for each transaction with an event column, a USD price column, and a moving average of USD price that averages the last 50 transactions.
4. Return all the NFT names and their average sale price in USD. Sort descending. Name the average column as average_price.
5. Return each day of the week and the number of sales that occurred on that day of the week, as well as the average price in ETH. Order by the count of transactions in ascending order.
6. Construct a column that describes each sale and is called summary. The sentence should include who sold the NFT name, who bought the NFT, who sold the NFT, the date, and what price it was sold for in USD rounded to the nearest thousandth.
 Here’s an example summary:
 “CryptoPunk #1139 was sold for $194000 to 0x91338ccfb8c0adb7756034a82008531d7713009d from 0x1593110441ab4c5f2c133f21b0743b2b43e297cb on 2022-01-14”
7. Create a view called “1919_purchases” and contains any sales where “0x1919db36ca2fa2e15f9000fd9cdc2edcf863e685” was the buyer.
8. Create a histogram of ETH price ranges. Round to the nearest hundred value. 
9. Return a unioned query that contains the highest price each NFT was bought for and a new column called status saying “highest” with a query that has the lowest price each NFT was bought for and the status column saying “lowest”. The table should have a name column, a price column called price, and a status column. Order the result set by the name of the NFT, and the status, in ascending order. 
10. What NFT sold the most each month / year combination? Also, what was the name and the price in USD? Order in chronological format. 
11. Return the total volume (sum of all sales), round to the nearest hundred on a monthly basis (month/year).
12. Count how many transactions the wallet "0x1919db36ca2fa2e15f9000fd9cdc2edcf863e685"had over this time period.
13. Create an “estimated average value calculator” that has a representative price of the collection every day based off of these criteria:
 - Exclude all daily outlier sales where the purchase price is below 10% of the daily average price
 - Take the daily average of remaining transactions
 a) First create a query that will be used as a subquery. Select the event date, the USD price, and the average USD price for each day using a window function. Save it as a temporary table.
 b) Use the table you created in Part A to filter out rows where the USD prices is below 10% of the daily average and return a new estimated value which is just the daily average of the filtered data.

## Key Features
1. Sales Summary
- Total sales during the dataset's timeframe.
- Top 5 most expensive transactions by USD price.

2. Advanced Metrics and Trends
- Moving averages of transaction prices for the last 50 sales.
- Average sale price per NFT.

3. Weekly and Daily Insights
- Sales count and average ETH price by day of the week.
- Exclusion of outliers to calculate daily representative values.

4. Custom Queries
- Summaries for individual transactions with seller, buyer, price, and date.
- Views for wallet-specific purchases (e.g., for wallet 0x1919...685).

5. Visualization and Insights
- Histogram of ETH price ranges.
- Highest and lowest price unioned query with status indicators.

6. Monthly and Yearly Analytics
- NFTs with the highest sales volume by month/year.
- Total monthly transaction volume (rounded).

7. Wallet Transactions
- Count of transactions by a specific wallet over the entire period.

## Instructions
1. Dataset: Ensure you have access to the Cryptopunks NFT sales dataset (CSV format).
2. SQL Environment: Use any SQL-compatible platform to execute the provided queries.

## How to Use This Repository
1. Clone the repository or download the SQL scripts.
2. Import the dataset into your SQL environment.
3. Run the provided queries sequentially or modify them as needed for deeper insights.
