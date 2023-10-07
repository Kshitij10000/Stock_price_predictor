# Stock_price_predictor
 A stock price predictor is a sophisticated tool used in the world of finance to anticipate future movements in stock prices. It serves as a valuable resource for investors, traders, and financial analysts who seek to make informed decisions in the stock market.
This code is a Streamlit web application that serves as a Stock Trend Predictor. Users can input a stock ticker symbol (e.g., 'AAPL' for Apple Inc.) to retrieve historical stock price data spanning the last 15 years. The code then provides various visualizations and predictions related to the stock's performance. Here's a breakdown of its functionality:

Title and User Input: The web application's title is set as "Stock Trend Predictor," and it includes a text input field where users can enter a stock ticker symbol.
Data Retrieval: Using the Yahoo Finance API (yfinance), the code downloads historical stock price data for the specified stock symbol over the last 15 years with daily intervals.
Data Description: It displays summary statistics of the downloaded data, such as mean, standard deviation, minimum, and maximum, providing an overview of the stock's historical performance.

Visualization 1: A line chart is generated to visualize the closing price of the stock over time.
Visualization 2: Another line chart is displayed, showing both the closing price and a 100-day moving average (MA) of the stock's price. This moving average helps users identify trends in the stock's performance.
Visualization 3: A third line chart displays the closing price along with both 100-day and 200-day moving averages. This chart allows users to assess longer-term trends in the stock's price.

Data Preprocessing: The code splits the historical data into training and testing sets, scaling the data to be in the range of 0 to 1 using Min-Max scaling.
Model Loading: A pre-trained machine learning model (loaded from 'stock_model.h5') is used for stock price prediction.
Testing and Prediction: The code prepares the data for testing by selecting the last 100 days of the training data and combining it with the testing data. It then iterates through the data to create input sequences for the model and makes stock price predictions.
Scaling Back: The predicted prices are scaled back to their original range to make meaningful comparisons with the actual stock prices.
Final Graph: A graph is displayed comparing the actual stock prices (blue) with the predicted prices (red) over time. This allows users to assess the model's performance in predicting stock price trends.

This code provides an interactive and informative way for users to explore historical stock data, visualize trends, and evaluate a pre-trained machine learning model's predictions for a specific stock symbol.
