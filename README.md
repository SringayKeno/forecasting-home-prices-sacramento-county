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
* [Analysis](#analysis) 
   * [All Home Types](#all-home-types)
   * [Condos and Coops](#condos-and-coops)
   * [1 Bedroom Homes](#1-bedroom-homes)
   * [2 Bedroom Homes](#2-bedroom-homes)
   * [3 Bedroom Homes](#3-bedroom-homes)
* [Links](#links)

</details>

### Project Overview


#### *This 10 part project is currently in progress thru Nov 2022. Using over 20 years of Zillow data, I identify the top 5 zip codes for home value in 9 different home catagories in Sacramento County. Then, I forecast those homes values and percentage increases out for the next 3 years using the SARIMA forecasting algorithm.* 



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

For more information regarding SARIMA, I suggest a visit to Jason Brownlee's, ['A Gentle Introduction to SARIMA for Time Series Forecasting in Python'](https://machinelearningmastery.com/sarima-for-time-series-forecasting-in-python/)

### Why Sarima

After working with another algorithm, long short term memory (LSTM) for housing inventory predictions, which model didn't perform as well as I would have liked it too, I did further research. That research lead me to the SARIMA model, which proved to do well with data sets like the one I use for the project. The SARIMA model is suitable for time series data with trend and/or seasonal components, which I believed this data set contained.

###  Resources 

*  Data Source: Data sourced from Zillow's research data page. I used [Zillow's Home Value Index (ZHVI)](https://www.zillow.com/research/data/) which is a  smoothed, seasonally adjusted measure of the typical home value and market changes across a given region and housing type. It reflects the typical value for homes in the 35th to 65th percentile range.
* Software: Jupyter Notebook, VScode, Google Slides, Git Bash, Slack
* Languages: Python 3.7
* Libraries: folium, itertools, json, math, pandas, pickle, matplotlib, numpy, scripts, seaborn, sklearn, statsmodel
* Machine Learning Models: SARIMA


###  Analysis

### All Home Types

#### Top Five Zip Codes for All Home Types

The top Five zip codes for the category, all types are listed below. Again, these zip codes were determined by looking at the differences between values (both in dollar and in percentage increases) month over month for the last 20 years. The zip codes below had the highest sum of those month to month difference, or in another words, deviated furthest from the county average. The Sacramento County zip code for all home types closest to the average was 95632 which is Galt, a city in southern Sacramento County.

![#2E86C1](https://via.placeholder.com/15/2E86C1/2E86C1.png) 95823 Parkway and Valley Hi/North Laguna Neighborhoods (Florin Rd and Hwy 99)<br/>
![#40E0D0](https://via.placeholder.com/15/40E0D0/40E0D0.png) 95630 Folsom California <br/>
![#99751b](https://via.placeholder.com/15/99751b/99751b.png) 95834 Natomas Crossing Neighborhood (Sacramento City)<br/>
![D8D051](https://via.placeholder.com/15/D8D051/D8D051.png) 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City)<br/>
![#A569BD](https://via.placeholder.com/15/A569BD/A569BD.png) 95829 Vinyard (Elk Grove)<br/>

#### Percent Forecast for All Home Types

Below is the forecasted increase/decrease for the 5 zip codes. We can see a decrease for all zip codes, but what is most interesting is what happens after the initial dip in 2022. 

Two zip codes in particular; ![#40E0D0](https://via.placeholder.com/15/40E0D0/40E0D0.png) 95630 Folsom California and ![D8D051](https://via.placeholder.com/15/D8D051/D8D051.png) 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City) are going to come out of the dip further and then see a slow increase upward again. Looking back over the timeline, the Old North Sacramento/Cal Expo Neighborhoods has seen the biggest flutuations in pricing. 

The other 3 zip codes; ![#A569BD](https://via.placeholder.com/15/A569BD/A569BD.png) 95829 Vinyard Area of Elk Grove (City) ![#99751b](https://via.placeholder.com/15/99751b/99751b.png) 95834 Natomas Crossing Neighborhood (Sacramento City) and ![#2E86C1](https://via.placeholder.com/15/2E86C1/2E86C1.png) 95823 Parkway and Valley Hi/North Laguna Neighborhoods (The Florin Rd and Hwy 99 area) will also see an increase albeit not to the extent of the previous two zip codes. Then, different from the other zip codes, those 3 zip codes will level off in mid 2024.

<img width="631" alt="Screenshot (534)" src="https://user-images.githubusercontent.com/102890151/191851151-8d64d524-30cd-431d-ae7c-d900962b2748.png">


#### Dollar Forecast for All Home Types

Below are the projected housing prices for the 5 zip codes. 

![#40E0D0](https://via.placeholder.com/15/40E0D0/40E0D0.png) Zip code 95630, which is City of Folsom has a higher price point than the other 4 zip codes. The Folsom zip code has proven to be more resilant to price declines than other Sacramento zip codes, and it is showing that again here in the next few years. This zip code will continue to separate itself further in price point even more in the near future. 

The 3 zips codes in the middle; ![#A569BD](https://via.placeholder.com/15/A569BD/A569BD.png) 95829 Vinyard (Elk Grove) ![#99751b](https://via.placeholder.com/15/99751b/99751b.png) 95834 Natomas Crossing Neighborhood (Sacramento City) ![#2E86C1](https://via.placeholder.com/15/2E86C1/2E86C1.png) 95823 Parkway and Valley Hi/North Laguna Neighborhoods (Florin Rd and Hwy 99) are almost uniform in their line shape. All 3 of these zip codes will continue to see decreases through mid 2025. The zip codes of 95829 Vinyard (Elk Grove) and 95834 Natomas Crossing Neighborhood (Sacramento City) will converge on price point mid-way through 2025.

![D8D051](https://via.placeholder.com/15/D8D051/D8D051.png) The Old North Sacramento/Cal Expo Neighborhood in Sacramento didn't see the highs the other 4 zip codes saw in 2022, but that zip code won't see the drop off that the other zip codes will see. The Old North Sacramento/Cal Expo Neighborhood then nearly levels off starting in 2024. This is something the other 4 zip codes are not projected to do. The Old North Sacramento/Cal Expo Neighborhoods will surpass the ![#2E86C1](https://via.placeholder.com/15/2E86C1/2E86C1.png) Parkway and Valley Hi/North Laguna Neighborhoods in price point in 2025.

<img width="693" alt="Screenshot (535)" src="https://user-images.githubusercontent.com/102890151/191851112-d12802dd-1b88-4c33-b904-2b2fdec76635.png">



### Condos and Coops

#### Top Five Zip Codes for Condos and Coops

![#2E86C1](https://via.placeholder.com/15/2E86C1/2E86C1.png) 95823 Parkway and Vally Hi/North Laguna Neighborhoods (Sacramento City) <br/>
![#40E0D0](https://via.placeholder.com/15/40E0D0/40E0D0.png) 95630 Folsom California <br/>
![#99751b](https://via.placeholder.com/15/99751b/99751b.png) 95811 Richards/part of Midtown/Southside Park Nieghborhoods (Sacramento City)<br/>
![D8D051](https://via.placeholder.com/15/D8D051/D8D051.png)  95814 Downtown Scramento <br/>
![#A569BD](https://via.placeholder.com/15/A569BD/A569BD.png) 95841 Amber Park/Garfield Hills Area (N Highlands/Sacramento Cities)<br/> 



#### Percent Forecast for Condos and Coops

<img width="574" alt="Screenshot (540)" src="https://user-images.githubusercontent.com/102890151/191881939-1984ddcf-683a-46ed-b2c4-21af7ea1feeb.png">

#### Dollar Forecast for Condos and Coops

<img width="634" alt="Screenshot (539)" src="https://user-images.githubusercontent.com/102890151/191881945-c225ba49-c309-486c-b249-65e2d5fa240c.png">

## <p align="center">1 Bedroom Homes</p>

The amount of data for one bedrooms was limited to only 11 zip codes, most of which were located in the city of Sacramento. In this catagory, instead of looking at just the top 5 zip codes, all 11 zip codes will be examined.

### <p align="center">Top Five Zip Codes for 1 Bedroom Homes</p>

Here are the top 5 zip codes for the 1 bedroom catagory. Again,'top' being defined as the zip codes having the highest sum of percentage increases from month to month over the last 10+ years or so. Data for this catagory started in March of 2009. Below are the top 5 zip codes.

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95628 Fair Oaks (City)</p>
<p align="center"><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95835 (north half) of North Natomas (Sacramento city)</p>
<p align="center"><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95833 South Natomas/Gardenland Neighborhoods (Sacramento city)</p>
<p align="center"><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95838 Robla, North Sacramento and Del Paso Heights Neighborhoods (Sacramento city)</p>
<p align="center"><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95820 Lawrence Park/Tahoe Park South Neighborhoods (Sacramento city)</p>. 

<!--PERCENT FORECAST 5-->
### <p align="center">Percent Forecast for 1 Bedroom Homes in Top 5 Zip Codes</p>

<img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> One bedrooms in Fair Oaks are going to level off (image below) right about zero in late 2023 telling us that home prices are going not show much movement at all. Additionally, zip codes <img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95835 (north half) of North Natomas and <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95838 in the Robla, North Sacramento and Del Paso Heights Neighborhoods are forcasted to flatline, but both in the negative percentage. The remaining two zip codes <img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95833 South Natomas/Gardenland Neighborhoods and <img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95820 Lawrence Park/Tahoe Park South Neighborhoods will see fluctutions, particulary South Natomas/Gardenland.

<img width="445" alt="Screenshot (569)" src="https://user-images.githubusercontent.com/102890151/193946471-f42542e8-eb51-410a-91ed-f3474b6bb30f.png">&#160;<img width="489" alt="Screenshot (572)" src="https://user-images.githubusercontent.com/102890151/193946643-2d3069bf-3757-44c3-88e5-312c51168659.png">

<!--DOLLAR FORECAST 5-->
### <p align="center">Dollar Forecast for 1 Bedroom Homes in Top 5 Zip Codes</p>

Only one of the top five zip codes (below) is forecasted to increase in price over the next few years. That zip code is <img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95833 the South Natomas/Gardenland Neighborhoods in the city of Sacramento. South Natomas/Gardenland Neighborhoods are located adjacent to downtown. Another zip code  <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95628 Fair Oaks (City) is forecasted to flatline. The remaining three zip codes, all in the city of Sacramento <img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95835 (northern half) of North Natomas <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" />  95838 Robla, North Sacramento and Del Paso Heights Neighborhoods and <img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95820 Lawrence Park/Tahoe Park South Neighborhoods are all forecasted to see declines in price.

<p align="center"><img width="575" alt="Screenshot (572)" src="https://user-images.githubusercontent.com/102890151/193946643-2d3069bf-3757-44c3-88e5-312c51168659.png"></p>

<!--DOLLAR FORECAST ALL-->
### <p align="center">One Bedroom Two Directions (A Clear Pattern)</p>

Before looking at the last 6 remaining zip codes for the one bedroom category, let's take a look at all 11 of the one bedroom zip codes together. There was a clear delination in the home price forecast (image below). <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> Homes in downtown Sacramento and adjacent neighborhoods all forecasted increases. On the other hand <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> one bedroom homes in neighborhoods further away from downtown, which generally had a lower price point to their downtown area counterparts in the past, all forecasted decreases. <br/>

<p align="center"><img width="575" alt="Screenshot (570)" src="https://user-images.githubusercontent.com/102890151/193970768-235d9b13-2d4b-46da-8bb7-38d6f720c28c.png">
</p><br>

<!--PERCENT AND PRICE FORECAST 6-->
### <p align="center">Percent and Price Forecast for Remaining 6 Zip Codes in 1 Bedroom Home Catagory</p>

<p align="center">There were a total of 11 zip codes in the one bedroom category. Let's examine the remaining 6 (listed below).<p/>

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95825 Sierra Oaks/Arden Arcade&#160;
<img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95815 Old North Sacramento&#160;
<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95818 LandPark/Curtis Park&#160;</p>
<p align="center"><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95816 Midtown/East Sacramento Neighborhoods&#160;
<img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95817 Oak Park/Fairgrounds&#160; 
 <img src="https://via.placeholder.com/15/3AB227/3AB227.png" width="10" height="10" /> 95811 Richards/New Era Park/Southside Park</p>
 
Five of the six remaining zip codes are adjacent to downtown Sacramento. Those zip codes are forecasted to fluctuate in the 0-1.5% increase range (a. below left) resulting in steady price increases (b. below right). The 6th zip code <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95825 Sierra Oaks/Arden Arcade, which is not adjacent to downtown, will see a steady -1.75% decline month to month (c. below left) resulting in a rather severe price drop forecasted at least until late 2025 (d . below right).

<img width="994" alt="Screenshot (583)" src="https://user-images.githubusercontent.com/102890151/194213112-a44c1351-4e93-40ac-af09-ea37e0237c30.png">

<p align="center">Again, percent forecast (below left) and price forecast (below right) for 1 Bedroom homes<p/>

<img width="994" alt="Screenshot (586)" src="https://user-images.githubusercontent.com/102890151/194327891-49b9443c-35f1-495f-a1ba-4517a06e5cc6.png">



[Back to Table of Contents](#forecasting-home-prices-in-sacramento-county-ca)
<br>


## <p align="center">2 Bedroom Homes</p>

### <p align="center">Top Five Zip Codes for 2 Bedroom Homes</p>

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Vally Hi/North Laguna Neighborhoods (Sacramento City)</p>
<p align="center"><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95819 East Sacramento Neighborhood (Sacramento City) </p>
<p align="center"><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95824 Lemon Hill Neighborhood (Sacramento City) </p>
<p align="center"><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95834 Natomas Crossing Neighborhood (Sacramento City)</p>
<p align="center"><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City)</p>. 


#### Percent Forecast for 2 Bedroom Homes

<img width="588" alt="Screenshot (541)" src="https://user-images.githubusercontent.com/102890151/191889544-58d8163b-d2ca-44b7-8c75-31d49b22bebb.png">


#### Dollar Forecast for 2 Bedroom Homes


<img width="629" alt="Screenshot (540)" src="https://user-images.githubusercontent.com/102890151/191891231-9f9a0752-b160-4d5a-923c-5292cec56b0c.png">


### 3 Bedroom Homes

#### Top Five Zip Codes for 3 Bedroom Homes

![#2E86C1](https://via.placeholder.com/15/2E86C1/2E86C1.png) 95823 Parkway and Vally Hi/North Laguna Neighborhoods (Sacramento City) <br/>
![#40E0D0](https://via.placeholder.com/15/40E0D0/40E0D0.png) 95673 Rio Linda California <br/>
![#99751b](https://via.placeholder.com/15/99751b/99751b.png) 95834 Natomas Crossing Neighborhood (Sacramento City) <br/>
![D8D051](https://via.placeholder.com/15/D8D051/D8D051.png)  95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City)<br/>
![#A569BD](https://via.placeholder.com/15/A569BD/A569BD.png) 95829 Vineyard Area (Elk Grove East) <br/> 


#### Percent Forecast for 3 Bedroom Homes

<img width="600" alt="Screenshot (544)" src="https://user-images.githubusercontent.com/102890151/192430788-df487bd5-0f10-45dd-855c-ec85eb48a5d2.png">


#### Dollar Forecast for 3 Bedroom Homes

<img width="600" alt="Screenshot (545)" src="https://user-images.githubusercontent.com/102890151/192430795-ef37107a-6ab4-4731-be12-8e32b447ef30.png">

### Links

 Jason Brownlee's, ['A Gentle Introduction to SARIMA for Time Series Forecasting in Python'](https://machinelearningmastery.com/sarima-for-time-series-forecasting-in-python/)


[back to top of page](#forecasting-home-prices-in-sacramento-county-ca)
