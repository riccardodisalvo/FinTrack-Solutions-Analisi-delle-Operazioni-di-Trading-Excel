## Project Overview

This project is designed to help you analyze and manipulate financial trading data. The provided Excel workbook consists of four sheets, each serving a different purpose in analyzing Bob's trades from January 1, 2021, onward. The goal is to explore the data, calculate insights, and visualize key metrics.

### Dataset Description

The dataset represents trading operations performed by Bob, with the following columns:

- **TradeID:** Unique identifier for the trade (8-digit number).
- **Stock Exchange:** Market where the trade occurred.
- **Region:** Country or confederation of the stock exchange.
- **Date Added:** Date when the trade was made (YYYY-MM-DD format).
- **Quantity:** Number of shares traded (bought/sold).
- **Buy Price:** Price per share when the trade was executed.
- **Date Sold:** Date when the trade was completed (YYYY-MM-DD format).
- **Sell Price:** Price per share at the time of sale.

## Excel Workbook Structure

The Excel workbook contains four sheets, each focused on different aspects of the trading data. Below are detailed descriptions for each sheet, including the required styles, contents, and tasks to be performed.

### 1. `My Trades`

- **Description:** This sheet contains the raw trading data with the required date formatting and additional calculations.
- **Contents:**
  - **TradeID:** Trade identifier.
  - **Stock Exchange:** Market of the trade.
  - **Region:** Country or confederation.
  - **Date Added:** Date of trade in DD/MM/YY format.
  - **Quantity:** Number of shares traded.
  - **Buy Price:** Price per share at purchase.
  - **Date Sold:** Date of trade completion in DD/MM/YY format.
  - **Sell Price:** Price per share at sale.

- **Styling:**
  - **Header Font:** Comics Sans MS, 12pt, blue color.
  - **Borders:** Double border around the header; single border around all other cells.
  - **Cell Background:** White with no extra borders or lines outside the table.

### 2. `Stock Exchanges`

- **Description:** This sheet summarizes trade activities by stock exchange and region.
- **Contents:**
  - **Region:** Country or confederation.
  - **Stock Exchange:** Market of the trade.
  - **Num of Trades:** Total number of trades per region.
  - **Mandatory to Pay Taxes:** Whether taxes must be paid based on the total quantity of trades in the region.
- **Tasks:**
  - **Pivot Table:** Create a pivot table to group markets by region and calculate the number of trades per region.
  - **Tax Calculation:** Add a column to indicate "yes" or "no" for tax payment requirements based on whether the total number of shares traded in a region is 67 or more.
  - **Styling:**
    - **Header Font:** Comics Sans MS, 12pt, blue color.
    - **Borders:** Double border around the header; single border around all other cells.
    - **Cell Background:** White with no extra borders or lines outside the table.

### 3. `Profit Insights`

- **Description:** This sheet provides a detailed analysis of trade profits and the duration of trades.
- **Contents:**
  - **TradeID:** References to all trades from the `My Trades` sheet.
  - **Duration:** Number of days between `Date Added` and `Date Sold`.
  - **Profit:** Calculated profit for each trade.
- **Tasks:**
  - **Profit Calculation:** Ensure that profit values are displayed in USD with 5 decimal places.
  - **Chart:** Create a bar chart to show the frequency distribution of trade durations.
  - **Commentary:** Add a text box to explain the chart and assess whether the duration of trades follows a normal distribution.
  - - **Tasks:**
  - Format the dates in `Date Added` and `Date Sold` columns to DD/MM/YY.
  - **Add the following columns:**
    - **Duration:** Calculate the number of days between `Date Added` and `Date Sold`.
    - **Profit:** Calculate the profit from each trade. Use the formula:
      ```
      Profit = (Sell Price - Buy Price) * Quantity
      ```
    - **Format:** Ensure that the `Profit` column is displayed as USD currency with 5 decimal places.
  - **Visualization:** Create a bar chart showing the frequency of different durations of trades.
  - **Commentary:** Add a text box below the bar chart to comment on the distribution of trade durations and discuss whether it follows a normal distribution.
  - 
- **Styling:**
  - **Header Font:** Comics Sans MS, 12pt, blue color.
  - **Borders:** Double border around the header; single border around all other cells.
  - **Cell Background:** White with no extra borders or lines outside the table.
  - 
  ### 4. `Number of Trades Exchanged`

- **Description:** This sheet analyzes the distribution of the number of trades across regions and calculates specific probabilities.
- **Contents:**
  - **Region:** Country or confederation.
  - **Number of Trades:** Count of trades per region.
- **Tasks:**
  - **Contingency Table:** Create a table to show the number of trades per region.
  - **Marginal Distributions:** Add marginal distributions for both regions and trade counts, with a grand total in the bottom-right corner.
  - **Probability Calculations:**
    - **UK Probability:** Calculate the probability that a randomly chosen trade was executed in any Asian state with a quantity = 1 units.
    - **Asian Probability:** Calculate the probability that a randomly chosen trade was executed in any Asian state with a quantity <= 8 units.
- **Styling:**
  - **Header Font:** Comics Sans MS, 12pt, blue color.
  - **Borders:** Double border around the header; single border around all other cells.
  - **Cell Background:** White with no extra borders or lines outside the table.
