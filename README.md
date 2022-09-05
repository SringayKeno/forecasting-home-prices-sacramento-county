## Forecasting Home Prices in Sacramento County CA 

![Screenshot (466)](https://user-images.githubusercontent.com/102890151/187573030-680d3f0d-80cb-4081-8edd-9bd179ec3963.png)

#### Forecasting Home Prices in Sacramento County California (years 2023-2025) using the SARIMA forecasting algorithm. 

Using over 20 years of Zillow data I forecasted homes values and percentage increases for homes in the 35th to 65th percentile range (medium range homes) in Sacramento County California using the SARIMA forecasting algorithm. 

#### SARIMA and ARIMA 

SARIMA or '*seasonal autoregressive integrated moving average'*, is an ARIMA or *auto-regressive integrated moving average* algorithm that supports univariate time series data with a seasonal component. Hense the 'S' for seasonal in front of ARIMA. SARIMA and ARIMA models look at the differences between values in the time series (autocorrelations or serial correlations in the data) . Autocorrelation represents the degree of similarity between a given time series and a lagged version of itself over successive time intervals. ARIMA/SARIMA models the data in 3 ways:

* the **AR** = A pattern based on past observations in the data (auto-regressive) 
* the **I** =The trend and seasonal (non-stationary) patterns in the data is accounted for (integrated) 
* the **MA** =Noise between consecutive time points (moving average) 

Auto-regressive integrated moving average, means it models by making the data set stationary through differencing using d (“integrated” part), pattern of past observations using p (“auto-regressive” part), and noise between consecutive time points using q (“moving average” part).

SARIMA contains four seasonal elements that are not part of ARIMA that must be configured; they are:

* P: Seasonal autoregressive order.
* D: Seasonal difference order.
* Q: Seasonal moving average order.
* m: The number of time steps for a single seasonal period.

#### For more information regarding SARIMA, I suggest a visit to Jason Brownlee's, [A Gentle Introduction to SARIMA for Time Series Forecasting in Python](https://machinelearningmastery.com/sarima-for-time-series-forecasting-in-python/)

### Resources
####  Data Source: Data sourced from Zillow's research data page. I used [Zillow's Home Value Index (ZHVI)](https://www.zillow.com/research/data/) which is a  smoothed, seasonally adjusted measure of the typical home value and market changes across a given region and housing type. It reflects the typical value for homes in the 35th to 65th percentile range.
#### Software: Jupyter Notebook, VScode, Google Slides, Git Bash, Slack
#### Languages: Python 3.7
#### Libraries: folium, itertools, json, math, pandas, pickle, matplotlib, numpy, scripts, seaborn, sklearn, statsmodel
#### Machine Learning Models: SARIMA

### Project

#### The project consisted of 4 parts:

* #### Part 1 [data cleaning and it's code can be found here](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_clean_sac.ipynb)
* #### Part 2 [initial data exploration and it's code can be found here](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explore/data_explore_sacr.ipynb)
* #### Part 3 [model evaluation and it's code can be found here](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/model_eval/sarima_model_evaluation_sac.ipynb)
* #### Part 4 [forecasting and it's code can be found here](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/forecast/sarima_forecast_sac.ipynb)

### The Results

#### In the [data exploration stage ](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explore/data_explore_sacr.ipynb) of the project I identified the top 5 Sacramento zip codes to hold their value best. This was determined by looking at the differences between values (both in dollar and in percentage increases) month over month for the last 20 years. These 5 zip codes deviated furthest from the County average.

#### Those 5 zip codes were:
* 95630 (Folsom CA) 
* 95818 (Land Park Neighborhood Sacramento)
* 95608 (Carmichael CA)
* 95632 (Galt CA) 
* and number 5 was zip code 95824 (Lemon Hill/FruitRidge Manor Neighborhoods of Sacramento) 

#### Your average!

The zip code that was closest to average of the County was zip code 95830 which is between Vinyard and Sloughhouse areas of the County.

The projected percent increases for the 5 zip codes thru 2025
<img width="500" alt="Screenshot (468)" src="https://user-images.githubusercontent.com/102890151/188361228-3a819873-146c-4e31-845f-862151983f75.png">


The projected Home values for the 5 zip codes thru 2025
<img width="542" alt="Screenshot (470)" src="https://user-images.githubusercontent.com/102890151/188361242-ab7b21e3-498e-4372-a7db-811928d4f714.png">
