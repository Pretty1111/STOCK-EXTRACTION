# STOCK-EXTRACTION
# Stock Data Graphing with Python

## Overview

This project involves creating a graphing function to visualize stock data for two companies, Tesla and GameStop. The function, `make_graph`, takes two dataframes as input: one containing stock data with columns Date and Close, and another containing revenue data with columns Date and Revenue. The function then plots two subplots in a single figure, displaying the historical share price and historical revenue of the respective company. The graph is limited to data up to June 2021.

## Dependencies

Before running the code, make sure you have the necessary libraries installed:

- Pandas
- Plotly
- Beautiful Soup (for web scraping)
- Requests (for web scraping)

## Instructions

### Define Graphing Function

The `make_graph` function takes three inputs: `stock_data`, `revenue_data`, and `stock`. 

- `stock_data`: A dataframe containing historical stock data for a company, with columns Date and Close.
- `revenue_data`: A dataframe containing historical revenue data for a company, with columns Date and Revenue.
- `stock`: A string representing the name of the stock (e.g., 'Tesla' or 'GameStop').

The function creates a subplot with two rows and one column. The first subplot displays the historical share price, and the second subplot displays the historical revenue. The function then sets axis labels and other layout properties before showing the graph.

### Question 1: Extract Tesla Stock Data

To extract Tesla stock data, use the `yfinance` library. Create a ticker object for Tesla using the Ticker function with the ticker symbol "TSLA". Then, use the `history` function to extract historical stock data for Tesla and store it in a dataframe named `tesla_data`. Set the period parameter to "max" to get information for the maximum amount of time.

### Question 2: Extract Tesla Revenue Data

To extract Tesla revenue data, use web scraping with the `requests` and `BeautifulSoup` libraries. Download the webpage containing the Tesla revenue data from "https://www.macrotrends.net/stocks/charts/TSLA/tesla/revenue" and save the text of the response as a variable named `html_data`. Then, parse the HTML data using BeautifulSoup.

Use BeautifulSoup or the `read_html` function to extract the table with Tesla Quarterly Revenue and store it into a dataframe named `tesla_revenue`. The dataframe should have columns Date and Revenue. Remove the comma and dollar sign from the Revenue column, and drop any null or empty rows from the dataframe. Display the last five rows of the `tesla_revenue` dataframe.

### Question 3: Extract GameStop Stock Data

To extract GameStop stock data, use the `yfinance` library similar to Question 1. Create a ticker object for GameStop using the Ticker function with the ticker symbol "GME". Then, use the `history` function to extract historical stock data for GameStop and store it in a dataframe named `gme_data`. Set the period parameter to "max" to get information for the maximum amount of time.

### Question 4: Extract GameStop Revenue Data

To extract GameStop revenue data, use web scraping similar to Question 2. Download the webpage containing the GameStop revenue data from "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/stock.html" and save the text of the response as a variable named `html_data`. Then, parse the HTML data using BeautifulSoup.

Use BeautifulSoup or the `read_html` function to extract the table with GameStop Quarterly Revenue and store it into a dataframe named `gme_revenue`. The dataframe should have columns Date and Revenue. Remove the comma and dollar sign from the Revenue column, and drop any null or empty rows from the dataframe. Display the last five rows of the `gme_revenue` dataframe.

### Question 5: Plot Tesla Stock Graph

Use the `make_graph` function to graph the Tesla stock data. Call the function with the `tesla_data` and `tesla_revenue` dataframes, and provide the title "Tesla" for the graph.

### Question 6: Plot GameStop Stock Graph

Use the `make_graph` function to graph the GameStop stock data. Call the function with the `gme_data` and `gme_revenue` dataframes, and provide the title "GameStop" for the graph.

Please note that the code provided assumes you have already installed the required libraries and imported them in your environment. Ensure that you run each section of the code sequentially to obtain the desired results.

Enjoy visualizing the stock data for Tesla and GameStop!
