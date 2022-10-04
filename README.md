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
   * [Analysis for All Home Types](#analysis-for-all-home-types)
   * [Analysis for Condos and Coops](#analysis-for-condos-and-coops)
   * [Analysis for 1 Bedroom Homes](#analysis-for-1-bedroom-homes)
   * [Analysis for 2 Bedroom Homes](#analysis-for-2-bedroom-homes)
   * [Analysis for 3 Bedroom Homes](#analysis-for-3-bedroom-homes)
* [Links](#links)


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

### Analysis for All Home Types

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



### Analysis for Condos and Coops

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

## Analysis for 1 Bedroom Homes

### Top Five Zip Codes for 1 Bedroom Homes


### Percent Forecast for 1 Bedroom Homes


<img width="575" alt="Screenshot (553)" src="https://user-images.githubusercontent.com/102890151/193726049-f63f1ec8-8123-4fb6-a305-6258aa30c899.png">

<img width="575" alt="Screenshot (556)" src="https://user-images.githubusercontent.com/102890151/193726077-f37ce987-0e2e-4f65-b1ad-549c1cb22a96.png">


### Dollar Forecast for 1 Bedroom Homes

There was a clear delination in the one bedroom home price forecast. <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> Homes in downtown Sacramento or adjacent neighborhoods all forecasted increases. <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> On the other hand, one bedroom homes in neighborhoods further away from downtown, which generally have a lower price point to downtown area one bedrooms, all forecasted decreases. <br/>


<img width="600" alt="Screenshot (562)" src="https://user-images.githubusercontent.com/102890151/193731779-8f004c64-21f9-4abe-93fb-4a394171db64.png">





<img width="575" alt="Screenshot (558)" src="https://user-images.githubusercontent.com/102890151/193728966-b63b70d1-9aef-41fc-bf7b-9663e04b230d.png">


<img width="575" alt="Screenshot (559)" src="https://user-images.githubusercontent.com/102890151/193728969-4c901280-5bb1-4b98-bafd-7699fd6d7206.png">

### Analysis for 2 Bedroom Homes

#### Top Five Zip Codes for 2 Bedroom Homes

![#2E86C1](https://via.placeholder.com/15/2E86C1/2E86C1.png) 95823 Parkway and Vally Hi/North Laguna Neighborhoods (Sacramento City) <br/>
![#40E0D0](https://via.placeholder.com/15/40E0D0/40E0D0.png) 95819 East Sacramento Neighborhood (Sacramento City)<br/>
![#99751b](https://via.placeholder.com/15/99751b/99751b.png) 95824 Lemon Hill Neighborhood (Sacramento City) <br/>
![D8D051](https://via.placeholder.com/15/D8D051/D8D051.png)  95834 Natomas Crossing Neighborhood (Sacramento City)<br/>
![#A569BD](https://via.placeholder.com/15/A569BD/A569BD.png) 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City)<br/> 


#### Percent Forecast for 2 Bedroom Homes

<img width="588" alt="Screenshot (541)" src="https://user-images.githubusercontent.com/102890151/191889544-58d8163b-d2ca-44b7-8c75-31d49b22bebb.png">


#### Dollar Forecast for 2 Bedroom Homes


<img width="629" alt="Screenshot (540)" src="https://user-images.githubusercontent.com/102890151/191891231-9f9a0752-b160-4d5a-923c-5292cec56b0c.png">


### Analysis for 3 Bedroom Homes

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
