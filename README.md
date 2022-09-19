## <center>Forecasting Home Prices in Sacramento County CA</center>

![Screenshot (466)](https://user-images.githubusercontent.com/102890151/187573030-680d3f0d-80cb-4081-8edd-9bd179ec3963.png)

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FSringayKeno%2Fforecasting-home-prices-sacramento-county&count_bg=%23DCBB79&title_bg=%23555555&icon=homeassistant.svg&icon_color=%F9E79F&title=page+visits&edge_flat=false)](https://hits.seeyoufarm.com)




## ![#d2ae6c](https://via.placeholder.com/15/d2ae6c/d2ae6c.png) Table of Contents 
<details>
  <summary>Click to expand or hide</summary>
  
* [Project Ovrview](#project-overview)
* [SARIMA and ARIMA](#sarima-and-arima)
* [Why SARIMA](#why-sarima)
* [Resources](#resources) 
* [Project Code in Python](#project)
* [The Results](#the-results) 
     * [All Home Types](#all-home-types)
* [The Forecast](#the-forecast) 

</details>

### Project Overview


#### *This 10 part project is currently in progress thru Nov 2022. Using over 20 years of Zillow data, I identify the top 5 zip codes for home value in 9 different home catagories in Sacramento County. Then, I forecast those homes values and percentage increases out for the next 3 years using the SARIMA forecasting algorithm.* 


##### Part 1
I start first by looking at average prices per zip code for all home types in Sacramento County. I then identify the 5 top zip codes. This is done by summing the month over month differences (both in price and percentage increase) over the last 20 years. Then using the machine learning algorithm SARMA or seasonal auto regressive integrated moving average, I predict what the average home values in those 5 zip codes will look like over the next 3 years. 

##### Parts 2-10
The next several parts of the project I do the same, but for a more specific home type categories; low tier priced homes, mid-tier, and then higher priced tier homes. Then, I will do the same for 1-5 bedroom homes. Finally, I take a look at a few other Sacramento zip codes of interest and see what they look like over the next few yearswith various home types.


### SARIMA and ARIMA 

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

#### For more information regarding SARIMA, I suggest a visit to Jason Brownlee's, ['A Gentle Introduction to SARIMA for Time Series Forecasting in Python'](https://machinelearningmastery.com/sarima-for-time-series-forecasting-in-python/)

### Why Sarima

After working with another algorithm, long short term memory (LSTM) for housing inventory predictions, which model didn't perform as well as I would have liked it too, I did further research. That research lead me to the SARIMA model, which proved to do well with data sets like the one I use for the project. The SARIMA model is suitable for time series data with trend and/or seasonal components, which I believed this data set contained.

###  Resources 

*  Data Source: Data sourced from Zillow's research data page. I used [Zillow's Home Value Index (ZHVI)](https://www.zillow.com/research/data/) which is a  smoothed, seasonally adjusted measure of the typical home value and market changes across a given region and housing type. It reflects the typical value for homes in the 35th to 65th percentile range.
* Software: Jupyter Notebook, VScode, Google Slides, Git Bash, Slack
* Languages: Python 3.7
* Libraries: folium, itertools, json, math, pandas, pickle, matplotlib, numpy, scripts, seaborn, sklearn, statsmodel
* Machine Learning Models: SARIMA


###  The Results

#### All Home Types

 In the [data exploration stage ](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explore/data_explore_sacr.ipynb) of the project I identified the top 5 Sacramento zip codes to hold their value best. This was determined by looking at the differences between values (both in dollar and in percentage increases) month over month for the last 20 years. These 5 zip codes deviated furthest from the County average.

#### Those 5 zip codes were:
* 95630 (Folsom CA) 
* 95818 (Land Park Neighborhood Sacramento City)
* 95608 (Carmichael CA)
* 95632 (Galt CA) 
* and number 5 was zip code 95824 (Lemon Hill/FruitRidge Manor Neighborhoods of Sacramento City) 

#### Your average!

The zip code that was closest to average of the County was zip code 95830 which is between Vinyard and Sloughhouse areas of the County. However, looking at zip code 95830, I realized that zip code should have been removed from the analysis. There were 2 issues. The first was not very much data. 95830 is a very small zip code (I was surprised it was it's own zip code) both in housing numbers and in square miles. 95830 consists of two ruralish subdivisions with about maybe 50 homes total. All or most of those homes would be above the 68th percentile which we were looking at here.  

When revisisting this and making correction, the 2nd closest to average zip code was 95834. 95834 is the North Natomas area of Sacramento (City)

####  The Forecast for All Home Types

 
##### The projected Home values for the 5 zip codes thru 2025.

<img width="542" alt="Screenshot (470)" src="https://user-images.githubusercontent.com/102890151/188361242-ab7b21e3-498e-4372-a7db-811928d4f714.png">

* Folsom (zip code 95630) which is already one of the highest price point zip codes will remain so and separate itself further from the other Sacramento County zip codes. 
* Med priced homes homes will level off in the Land Park neighborhood (95818) in Sacramento (city) and Carmichael (95608), both areas with older housing stock and higher value (above our 68 pertile looked at here). 
* Galt (95632) will continue to rise, but at a much more more modest rate. 
* Zip code 95824 (Lemon Hill/FruitRidge Manor Neighborhoods of Sacramento City) will continue to show increase in home values.

##### Code for all home types:

* Part 1 [data cleaning and it's code can be found here](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_clean_sac.ipynb)
* Part 2 [initial data exploration and it's code can be found here](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explore/data_explore_sacr.ipynb)
* Part 3 [model evaluation and it's code can be found here](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/model_eval/sarima_model_evaluation_sac.ipynb)
* Part 4 [forecasting and it's code can be found here](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/forecast/sarima_forecast_sac.ipynb)

[back to top of page](#forecasting-home-prices-in-sacramento-county-ca)
