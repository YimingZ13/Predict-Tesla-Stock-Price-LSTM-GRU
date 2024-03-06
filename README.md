# Predict Tesla's Stock Price with LSTM and GRU

## Table of Contents
1. [Introduction](#Introduction)
2. [File Structure](#FileStructure)
3. [Installing](#Installing)
4. [Feature Documentations](#FeatureDocumentations)
5. [Key Results](#KeyResults)
6. [Future Improvement](#FutureImprovement)
7. [Authors](#Authors)
8. [License](#License)

<a name="Introduction"></a>
## Introduction
Welcome to the Tesla Stock Price Prediction project! This repository contains a detailed machine learning model that utilizes Long Short-Term Memory (LSTM) and Gated Recurrent Unit (GRU) neural networks to forecast the future stock prices of Tesla Inc. (TSLA). Our goal is to demonstrate how advanced deep learning techniques can be applied to financial time series data to make informed predictions.

The stock market is known for its volatile and unpredictable nature, making it a prime candidate for the application of deep learning models to understand and forecast trends. In this project, we focus on Tesla Inc., an American electric vehicle and clean energy company that has shown remarkable growth and interest among investors.

We leverage LSTM and GRU, two powerful types of recurrent neural networks (RNNs), known for their ability to capture temporal dependencies and patterns in time-series data. By analyzing historical stock price movements, our model aims to predict future prices, helping investors and enthusiasts make more informed decisions.

The [original datasets](https://www.kaggle.com/datasets/varpit94/tesla-stock-data-updated-till-28jun2021), encapsulates TSLA price from 2010-06-29 to 2022-03-24.

<a name="FileStructure"></a>
## File Structure
Each of the following project steps is completed in a separate notebook:
- [Raw Stock Data](https://github.com/YimingZ13/Predict-Tesla-Stock-Price-LSTM-GRU/blob/main/TSLA.csv): `TSLA.csv`
- [Data Cleaning and EDA](https://github.com/YimingZ13/Predict-Tesla-Stock-Price-LSTM-GRU/blob/main/tesla_cleaning_EDA.ipynb): `tesla_cleaning_EDA.ipynb`
- [Data Preprocessing and Modelling](https://github.com/YimingZ13/Predict-Tesla-Stock-Price-LSTM-GRU/blob/main/tesla_modelling.ipynb): `tesla_modelling.ipynb`

<a name="Installing"></a>
## Installing
There are no special packages needed for this project, most of packages come with the Anaconda distribution of Python 3.

<a name="FeatureDocumentations"></a>
## Feature Documentations
`2021_donnees_ouvertes.csv`:
- `Date`: Date (yyyy-MM-dd)
- `Open`: Price from the first transaction of a trading day
- `High`: Maximum price in a trading day
- `Low`:  Minimum price in a trading day
- `Close`: Price from the last transaction of a trading day
- `Adj Close`: Closing price adjusted to reflect the value after accounting for any corporate actions (Target Variable)
- `Volume`: Number of units traded in a day

<a name="KeyResults"></a>
## Key Results
- The best performed model was trained on the data from 2019-11-01 to 2021-09-30. The Root Mean Square Error (RMSE) of 19.87 indicates that, on average, the model's predictions are approximately $19.87 away from the actual stock prices. Given the price scale on the y-axis, an RMSE of 19.87 can be considered relatively small, especially during periods where the stock price exhibits high volatility and large price swings.
- The model seems capable of capturing both the trend and, to some extent, the volatility of the closing price. The predictions on the test captures the general trend and volatility.
- Despite the overall good performance, careful attention should be given to any small deviations, especially if the model predictions start to consistently lag behind or overshoot actual values. This isn't evident in the provided graph but is something to monitor with a more granular analysis. The excellent alignment between predictions and actual values in both validation and test phases suggests that overfitting is likely not a concern here, assuming the validation and test sets are appropriately challenging and representative of the problem space.
- The graph of the predictions into the next 90 consecutive days, shows significant volatility in the end of the dataset, especially in the period of rapid growth. The model's predictions seem to smooth out this volatility, which is common in many predictive models that may struggle to capture sharp, short-term fluctuations in stock prices. Without seeing the exact metrics (e.g., RMSE, MAE) used to evaluate the model, it's challenging to quantify how well the model fits the historical data. However, visually, it seems to follow the general trend well, which is promising for its potential utility.

<a name="FutureImprovement"></a>
## Future Improvement
-  Implementing a dynamic model that adjusts its predictions based on new data points received daily could enhance its predictive accuracy over time.
-  Due to stock market's unpredicted nature, implementing a sentiment analysis model as a complement to the LSTM (Long Short-Term Memory) model can significantly enhance its predictive power. Sentiment analysis leverages natural language processing (NLP) techniques to understand the sentiment behind textual data from various sources like news headlines, social media, financial reports, and analyst ratings, which can have a profound impact on stock prices:
  - Social Media: Collect data from platforms like Twitter and Reddit where financial discussions occur. Use APIs like Tweepy for Twitter to gather tweets related to Tesla.
  - News Articles: Scrape news articles and financial news websites for Tesla-related content.
Financial Reports: Quarterly and annual reports from Tesla can provide insights into the company's performance.

<a name="Authors"></a>
## Authors
Yiming Zhao | [LinkedIn](https://www.linkedin.com/in/yiming-zhao13/)

<a name="License"></a>
## License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

The project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
