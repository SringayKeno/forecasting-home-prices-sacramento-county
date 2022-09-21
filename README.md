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
   * [The Results for All Home Types](#results-for-all-home-types)
     * [Five Zip Codes](#five-zip-codes)
     * [Percent Forecast](#percent-forecast)
     * [Dollar Forecast](#dollar-forecast)
  
   * [The Results for Single Family Homes](#the-results-for-single-family-homes)
     

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

#### Results for All Home Types

##### Five Zip Codes

The top Five zip codes for the category, all types are listed below. Again, these zip codes were determined by looking at the differences between values (both in $dollar and in %percentage increases) month over month for the last 20 years. The zip codes below had the highest sum of those month to month difference, or in another words, deviated furthest from the county average. The Sacramento County zip code for all home types closest to the average was 95632 which is Galt, a city in southern Sacramento County.

- 95630 Folsom California
- 95829 Vinyard (Elk Grove)
- 95834 Natomas Crossing Neighborhood (Sacramento City)
- 95823 Parkway and Valley Hi/North Laguna Neighborhoods (Florin Rd and Hwy 99)
- 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City)


##### Percent Forecast

Below is the forecasted increase/decrease for the 5 zip codes. We can see a decrease for all zip codes, but what is most interesting is what happens after the initial dip in 2022. Two zip codes in particular; 95630 (aqua)Folsom California and 95815 (olive) Old North Sacramento/Cal Expo Neighborhoods (Sacramento City) are going to come out of the dip further and then see a slow increase upward again. The other 3 zip codes; 95829 (in purple) Vinyard Area of Elk Grove (City), 95834 (gray) Natomas Crossing Neighborhood (Sacramento City) and 95823 (dark blue) Parkway and Valley Hi/North Laguna Neighborhoods (The Florin Rd and Hwy 99 area) will also see an increase albeit not to the extent of the previous two zip codes. Then, different from the other zip codes, those 3 zip codes will level off in mid 2024.

<img width="497" alt="Screenshot (528)" src="https://user-images.githubusercontent.com/102890151/191414523-89132e7c-5042-4255-a376-4bcee0fbee5f.png">

###### Expanded Legend
- 95630 (aqua) Folsom California
- 95829 (purple) Vinyard (Elk Grove)
- 95834 (gray) Natomas Crossing Neighborhood (Sacramento City)
- 95823 (dark blue above) Parkway and Valley Hi/North Laguna Neighborhoods (Florin Rd and Hwy 99)
- 95815 (olive) Old North Sacramento/Cal Expo Neighborhoods (Sacramento City)

##### Dollar Forecast

 <img width="538" alt="Screenshot (529)" src="https://user-images.githubusercontent.com/102890151/191414556-6cc0a47c-1130-4de8-a880-9a6bd2b04dca.png">

Above are the projected housing prices for the 5 zip codes. Zip code 95630 (aqua color) which is City of Folsom California has a higher price point than the other 4 zip codes and clearly has separated itself in the past will continue to do so even more in the near future. The Folsom zip code has long proven to be more resilant to price declines than other Sacramento zip codes, and it is showing that again here in the next few years. The Old North Sacramento/Cal Expo Neighborhood in Sacramento (olive) didn't see the highs the other 4 zip codes saw in 2022, but that zip code won't see the drop off that the other zip codes will see. The Old North Sacramento/Cal Expo Neighborhood then nearly levels off starting in 2024. This is something the other 4 zip codes are not projected to do. The remaining 3 zips codes;  95829 (purple) 95834 (gray) 95823 (dark blue) are almost uniform in their line shape. All 3 of these zip codes will continue to see decreases through mid 2025.

Two Sacramento City neighborhoods will actually switch places in 2024. The average home price in zip code 95823 (dark blue) Parkway and Valley Hi/North Laguna Neighborhoods will drop below that of the Old North Sacramento/Cal Expo Neighborhoods (in olive).

#### The Results for Single Family Homes

[back to top of page](#forecasting-home-prices-in-sacramento-county-ca)
