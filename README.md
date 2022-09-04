# Forecasting Home Prices in Sacramento County CA

![Screenshot (466)](https://user-images.githubusercontent.com/102890151/187573030-680d3f0d-80cb-4081-8edd-9bd179ec3963.png)

#### Forecasting Home Prices in Sacramento County California (years 2023-2025) using the SARIMA forecasting method.  Auto-Regressive Integrated Moving Average or ARIMA models look at the differences between values in the time series (autocorrelations or serial correlations in the data) . SARIMA or seasonal autoregressive integrated moving average, supports univariate time series data with a seasonal component. 

#### For more information regarding SARIMA, I suggest a visit to Jason Brownlee's [A Gentle Introduction to SARIMA for Time Series Forecasting in Python](https://machinelearningmastery.com/sarima-for-time-series-forecasting-in-python/)

### Resources
#### * Data Source: Data sourced from Zillow's research data page. I used [Zillow's Home Value Index (ZHVI)](https://www.zillow.com/research/data/) which is a  smoothed, seasonally adjusted measure of the typical home value and market changes across a given region and housing type. It reflects the typical value for homes in the 35th to 65th percentile range.
#### Software: Jupyter Notebook, VScode, Google Slides, Git Bash, Slack
#### Languages: Python 3.7
#### Libraries: folium, itertools, json, math, pandas, pickle, matplotlib, numpy, scripts, seaborn, sklearn, statsmodel, urllib
#### Machine Learning Models: SARIMA

### Project

#### The project consisted of 4 parts:

* #### Part 1 data cleaning code can be found [here](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_clean_sac.ipynb)
* #### Part 2 initial data exploration and it's code can be found [here](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explore/data_explore_sacr.ipynb)
* #### Part 3 model evaluation and it's code can be found [here](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/model_eval/sarima_model_evaluation_sac.ipynb)
* #### Part 4 Forecasting and it's code can be found [here](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/forecast/sarima_forecast_sac.ipynb)

### The Results

#### In the [data exploration stage ](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explore/data_explore_sacr.ipynb) of the project I identified the top 5 Sacramento zip codes to hold their value best. The 5 zip codes month over month for the last 20 years had the biggest percentage increases and dollar increase.

#### Those 5 zip codes were 95630 (Folsom CA), 95818 (Land Park Neighborhood Sacramento), 95608 (Carmichael CA), 95632 (Galt CA) and number 5 was zip code 95824 (Lemon Hill/FruitRidge Manor Neighborhoods). 