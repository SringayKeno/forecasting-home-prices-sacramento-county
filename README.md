## <center>Forecasting Home Prices in Sacramento County CA</center>

![Screenshot (466)](https://user-images.githubusercontent.com/102890151/187573030-680d3f0d-80cb-4081-8edd-9bd179ec3963.png)

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FSringayKeno%2Fforecasting-home-prices-sacramento-county&count_bg=%23DCBB79&title_bg=%23555555&icon=homeassistant.svg&icon_color=%F9E79F&title=page+visits&edge_flat=false)](https://hits.seeyoufarm.com)




## ![#d2ae6c](https://via.placeholder.com/15/d2ae6c/d2ae6c.png) Table of Contents 
<details>
  <summary>Click to expand or hide</summary>
  
* [Project Overview](#project-overview)
* [SARIMA and ARIMA](#sarima-and-arima)
* [Why SARIMA](#why-sarima)
* [Resources](#resources) 
* [The Results](#the-results) 
   * [All Home Types](#all-home-types)
     * [Forecast For All Home Types](#the-forecast-for-all-home-types)
     

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

The top Five zip codes are listed below. These zip codes were determined by looking at the differences between values (both in dollar and in percentage increases) month over month for the last 20 years. THe below zip codes had the highest sum total, or in another words deviated furthest from the county average.

- 95630 Folsom California
- 95829 Vinyard (Elk Grove)
- 95834 Natomas Crossing Neighborhood (Sacramento City)
- 95823 Parkway and Valley Hi/North Laguna Neighborhoods (Florin Rd and Hwy 99)
- 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City)

#### The Average

The Sacramento County zip code for all home types closest to the average was 95632 which is the city of Galt in southern Sacramento County.
  
####  The Forecast for All Home Types

Below is the forecasted increase/decrease for the 5 zip codes. WE can see a decrease for all zip codes, but what is most interesting is what happens after the initial dip in 2022. Some areas are forecasted to level off after showing an increase such as zip codes 95630 (Folsom Ca) and 95823 (Parkway and Valley Hi/North Laguna Neighborhoods in Sacramento (City). The other 3 zip codes are projected to continue upward thru mid 2025. 

<img width="581" alt="Screenshot (523)" src="https://user-images.githubusercontent.com/102890151/191389624-d96b6ef8-2756-4391-9334-c5202f874bc7.png">

##### Expanded Legend
- 95630 (aqua) Folsom California
- 95829 (purple) Vinyard (Elk Grove)
- 95834 (gray) Natomas Crossing Neighborhood (Sacramento City)
- 95823 (dark blue above) Parkway and Valley Hi/North Laguna Neighborhoods (Florin Rd and Hwy 99)
- 95815 (olive) Old North Sacramento/Cal Expo Neighborhoods (Sacramento City)

 <img width="605" alt="Screenshot (522)" src="https://user-images.githubusercontent.com/102890151/191389603-a147225a-13b2-4a9d-8573-06ca973b6e82.png">
 
 Above is the projected housing prices for the 5 zip codes. Zip code 95630 (aqua color) which has a higher price point than the other 4 zip codes and clearly separated itself will see the steepest drops in home prices. Zip code 95823 will also see a similar decline. In olive color, The Old North Sacramento/Cal Expo Neighborhoods (Sacramento City) and Natomas Crossing Neighborhood (Sacramento City) shown in gray, show the least decline with the The Old North Sacramento/Cal Expo Neighborhood almost leveling off.


[back to top of page](#forecasting-home-prices-in-sacramento-county-ca)
