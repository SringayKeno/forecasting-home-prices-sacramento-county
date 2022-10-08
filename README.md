<!--TITLE TITLE TITLE-->
## <center>Forecasting Home Prices in Sacramento County CA</center>

<!--OPENING IMAGE OPENING IMAGE-->
![Screenshot (466)](https://user-images.githubusercontent.com/102890151/187573030-680d3f0d-80cb-4081-8edd-9bd179ec3963.png)

<!--HIT COUNTER HIT HIT HIT-->
[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FSringayKeno%2Fforecasting-home-prices-sacramento-county&count_bg=%23DCBB79&title_bg=%23555555&icon=homeassistant.svg&icon_color=%F9E79F&title=page+visits&edge_flat=false)](https://hits.seeyoufarm.com)



<!--TABLE OF CONTENTS TABLE TABLE-->
### <img src="https://via.placeholder.com/15/d2ae6c/d2ae6c.png" width="10" height="10" /> Table of Contents 
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
   * [4 Bedroom Homes](#4-bedroom-homes)
   * [5 Bedroom Homes](#5-bedroom-homes)
   * [Mather and Rancho Cordova CA](#mather-and-rancho-cordova-ca)
* [Links](#links)

</details>

<!--PROJECT OVERVIEW-->
## <p align="center">Project Overview<p/>


#### *This 10 part project is currently in progress thru Nov 2022. Using over 20 years of Zillow data, I identify the top 5 zip codes for home value in 9 different home catagories in Sacramento County. Then, I forecast those homes values and percentage increases out for the next 3 years using the SARIMA forecasting algorithm.*

<!--SARIMA AND ARIMA-->
## <p align="center">SARIMA and ARIMA<p/>

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

<!--WHY SARIMA WHY-->
## <p align="center">Why Sarima<p/>

After working with another algorithm, long short term memory (LSTM) for housing inventory predictions, which model didn't perform as well as I would have liked it too, I did further research. That research lead me to the SARIMA model, which proved to do well with data sets like the one I use for the project. The SARIMA model is suitable for time series data with trend and/or seasonal components, which I believed this data set contained.

<!--RESOURCES RESOURCES-->
##  <p align="center">Resources<p/> 

*  Data Source: Data sourced from Zillow's research data page. I used [Zillow's Home Value Index (ZHVI)](https://www.zillow.com/research/data/) which is a  smoothed, seasonally adjusted measure of the typical home value and market changes across a given region and housing type. It reflects the typical value for homes in the 35th to 65th percentile range.
* Software: Jupyter Notebook, VScode, Google Slides, Git Bash, Slack
* Languages: Python 3.7
* Libraries: folium, itertools, json, math, pandas, pickle, matplotlib, numpy, scripts, seaborn, sklearn, statsmodel
* Machine Learning Models: SARIMA

<!--ANALYSIS ANALYSIS-->
## <p align="center">Analysis<p/> 

<!--ALL TYPES-->
## <p align="center">All Home Types</p>

<!--ALL TYPES TOP 5-->
### <p align="center">Top Five Zip Codes for All Home Types<p/>

The top Five zip codes for the category, all types are listed below. Again, these zip codes were determined by looking at the differences between values (both in dollar and in percentage increases) month over month for the last 20 years. The zip codes below had the highest sum of those month to month difference, or in another words, deviated furthest from the county average. The Sacramento County zip code for all home types closest to the average was 95632 which is Galt, a city in southern Sacramento County.

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Valley Hi/North Laguna Neighborhoods (Florin Rd and Hwy 99)</p>
<p align="center"><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95630 Folsom California </p>
<p align="center"><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95834 Natomas Crossing Neighborhood (Sacramento City) </p>
<p align="center"><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City) </p>
<p align="center"><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95829 Vinyard (Elk Grove) </p>



<!--PERCENT and Price FORECAST ALL HOME TYPES--><!--PERCENT and Price FORECAST ALL HOME TYPES--><!--PERCENT and Price FORECAST ALL HOME TYPES-->
### <p align="center">Percent and Price Forecast for Condos All Home Types</p>


<img width="462" alt="Screenshot (617)" src="https://user-images.githubusercontent.com/102890151/194723830-c5a18dd2-7da6-4bf6-b8f9-32877fc6f1af.png">&#160;<img width="525" alt="Screenshot (618)" src="https://user-images.githubusercontent.com/102890151/194723832-d2e18148-5b60-4fd8-a4f8-e4a295cc67bc.png">



Below is the forecasted increase/decrease for the 5 zip codes. We can see a decrease for all zip codes, but what is most interesting is what happens after the initial dip in 2022. 

Two zip codes in particular; ![#40E0D0](https://via.placeholder.com/15/40E0D0/40E0D0.png) 95630 Folsom California and ![D8D051](https://via.placeholder.com/15/D8D051/D8D051.png) 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City) are going to come out of the dip further and then see a slow increase upward again. Looking back over the timeline, the Old North Sacramento/Cal Expo Neighborhoods has seen the biggest flutuations in pricing. 

The other 3 zip codes; ![#A569BD](https://via.placeholder.com/15/A569BD/A569BD.png) 95829 Vinyard Area of Elk Grove (City) ![#99751b](https://via.placeholder.com/15/99751b/99751b.png) 95834 Natomas Crossing Neighborhood (Sacramento City) and ![#2E86C1](https://via.placeholder.com/15/2E86C1/2E86C1.png) 95823 Parkway and Valley Hi/North Laguna Neighborhoods (The Florin Rd and Hwy 99 area) will also see an increase albeit not to the extent of the previous two zip codes. Then, different from the other zip codes, those 3 zip codes will level off in mid 2024.



Below are the projected housing prices for the 5 zip codes. 

![#40E0D0](https://via.placeholder.com/15/40E0D0/40E0D0.png) Zip code 95630, which is City of Folsom has a higher price point than the other 4 zip codes. The Folsom zip code has proven to be more resilant to price declines than other Sacramento zip codes, and it is showing that again here in the next few years. This zip code will continue to separate itself further in price point even more in the near future. 

The 3 zips codes in the middle; ![#A569BD](https://via.placeholder.com/15/A569BD/A569BD.png) 95829 Vinyard (Elk Grove) ![#99751b](https://via.placeholder.com/15/99751b/99751b.png) 95834 Natomas Crossing Neighborhood (Sacramento City) ![#2E86C1](https://via.placeholder.com/15/2E86C1/2E86C1.png) 95823 Parkway and Valley Hi/North Laguna Neighborhoods (Florin Rd and Hwy 99) are almost uniform in their line shape. All 3 of these zip codes will continue to see decreases through mid 2025. The zip codes of 95829 Vinyard (Elk Grove) and 95834 Natomas Crossing Neighborhood (Sacramento City) will converge on price point mid-way through 2025.

![D8D051](https://via.placeholder.com/15/D8D051/D8D051.png) The Old North Sacramento/Cal Expo Neighborhood in Sacramento didn't see the highs the other 4 zip codes saw in 2022, but that zip code won't see the drop off that the other zip codes will see. The Old North Sacramento/Cal Expo Neighborhood then nearly levels off starting in 2024. This is something the other 4 zip codes are not projected to do. The Old North Sacramento/Cal Expo Neighborhoods will surpass the ![#2E86C1](https://via.placeholder.com/15/2E86C1/2E86C1.png) Parkway and Valley Hi/North Laguna Neighborhoods in price point in 2025.



<!--CONDOS AND COOPS-->
## <p align="center">Condos and Coops</p>

<!--TOP 5 FOR FORECAST CONDOS-->
### <p align="center">Top Five Zip Codes for Condos and Coops</p>

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Vally Hi/North Laguna Neighborhoods (Sacramento City)</p>
<p align="center"><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95630 Folsom California </p>
<p align="center"><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95811 Richards/part of Midtown/Southside Park Nieghborhoods (Sacramento City) </p>
<p align="center"><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95814 Downtown Scramento </p>
<p align="center"><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95841 Amber Park/Garfield Hills Area (N Highlands/Sacramento Cities)</p>



<!--PERCENT and Price FORECAST CONDOS--><!--PERCENT and Price FORECAST CONDOS--><!--PERCENT and Price FORECAST CONDOS-->
### <p align="center">Percent and Price Forecast for Condos and Coops</p>


<img width="462" alt="Screenshot (615)" src="https://user-images.githubusercontent.com/102890151/194723812-75863d71-b3e0-4d68-b306-2874e6f15088.png">&#160;<img width="525" alt="Screenshot (616)" src="https://user-images.githubusercontent.com/102890151/194723816-28b117d0-339d-443e-ba41-c75e05ed8a53.png">






<!--ONE BEDROOM HOMES-->
## <p align="center">1 Bedroom Homes</p>

The amount of data for one bedrooms was limited to only 11 zip codes, most of which were located in the city of Sacramento. In this catagory, instead of looking at just the top 5 zip codes, all 11 zip codes will be examined.

<!--TOP 5 ONE BEDROOM-->
### <p align="center">Top Five Zip Codes for 1 Bedroom Homes</p>

Here are the top 5 zip codes for the 1 bedroom catagory. Again,'top' being defined as the zip codes having the highest sum of percentage increases from month to month over the last 10+ years or so. Data for this catagory started in March of 2009. Below are the top 5 zip codes.

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95628 Fair Oaks (City)</p>
<p align="center"><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95835 (north half) of North Natomas (Sacramento city)</p>
<p align="center"><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95833 South Natomas/Gardenland Neighborhoods (Sacramento city)</p>
<p align="center"><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95838 Robla, North Sacramento and Del Paso Heights Neighborhoods (Sacramento city)</p>
<p align="center"><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95820 Lawrence Park/Tahoe Park South Neighborhoods (Sacramento city)</p>


<!--DOLLAR FORECAST 5 ONE BEDROOM-->
### <p align="center">Percent and Price Forecast for 1 Bedroom Homes in Top 5 Zip Codes</p>

Only one of the top five zip codes is forecasted to increase in price over the next few years. That zip code <img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95833 the South Natomas/Gardenland Neighborhoods, which is located adjacent to downtown will fluctuate between .25 and 1.75 (a1. below) in month to month percent increases. The price forecast (a2. below) for 95833 looks much like it's historical past since 2014 as it continues to climb.

<img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> The 95628 zip code, Fair Oaks (City) is not going up or down, but rather is forecasted to flatline about at the 0% mark (b1.  below) resulting in little to no price changes at least until early 2026 (b2. below). 

<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" />  95838 The Robla, North Sacramento and Del Paso Heights Neighborhoods, which are in the city of Sacramento will see month to month percent decreases around the -1.25 rate (c1. below) and price reductions (c2. below) that will take 1 bedrooms in that zip code back to 2018 values over the next few years.

The remaining two zip codes, all in the city of Sacramento <img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95835 (northern half) of North Natomas <img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95820 Lawrence Park/Tahoe Park South Neighborhoods are all forecasted to see declines in price.

<img width="994" alt="Screenshot (587)" src="https://user-images.githubusercontent.com/102890151/194338237-94c413ce-6998-4e0b-9912-adb3c185ba14.png">

<!--DOLLAR FORECAST ALL ZIP CODES ONE BEDROOM-->
### <p align="center">One Bedroom Two Directions (A Clear Pattern)</p>

Before looking at the last 6 remaining zip codes for the one bedroom category, let's take a look at all 11 of the one bedroom zip codes together. There was a clear delination in the home price forecast (image below). <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> Homes in downtown Sacramento and adjacent neighborhoods all forecasted increases. On the other hand <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> one bedroom homes in neighborhoods further away from downtown, which generally had a lower price point to their downtown area counterparts in the past, all forecasted decreases. <br/>

<p align="center"><img width="475" alt="Screenshot (570)" src="https://user-images.githubusercontent.com/102890151/193970768-235d9b13-2d4b-46da-8bb7-38d6f720c28c.png">
</p>

<!--PERCENT AND PRICE FORECAST 6 ONE BEDROOM-->
### <p align="center">Percent and Price Forecast for Remaining 6 Zip Codes in 1 Bedroom Home Catagory</p>

<p align="center">There were a total of 11 zip codes in the one bedroom category. Let's examine the remaining 6 (listed below).<p/>

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95825 Sierra Oaks/Arden Arcade<br>
<img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95815 Old North Sacramento<br>
<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95818 LandPark/Curtis Park<br>
<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95816 Midtown/East Sacramento Neighborhoods<br>
<img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95817 Oak Park/Fairgrounds<br>
<img src="https://via.placeholder.com/15/3AB227/3AB227.png" width="10" height="10" /> 95811 Richards/New Era Park/Southside Park<p/>
 
Five of the six remaining zip codes are adjacent to downtown Sacramento. Those zip codes are forecasted to fluctuate in the 0-1.5% increase range (a1. below left) resulting in steady price increases (a2. below right). The 6th zip code <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95825 Sierra Oaks/Arden Arcade, which is not adjacent to downtown, will see a steady -1.75% decline month to month (b1. below left) resulting in a forecasted price drop at least until late 2025 (b2. below right).

<img width="994" alt="Screenshot (584)" src="https://user-images.githubusercontent.com/102890151/194337926-8a933f81-5383-4135-88b3-08239025ab87.png">

<p align="center">Again, percent forecast (below left) and price forecast (below right) for 1 Bedroom homes<p/>

<img width="994" alt="Screenshot (586)" src="https://user-images.githubusercontent.com/102890151/194327891-49b9443c-35f1-495f-a1ba-4517a06e5cc6.png">

[Back to Table of Contents](#forecasting-home-prices-in-sacramento-county-ca)
<br>

<!--TWO BEDROOM-->
## <p align="center">2 Bedroom Homes</p>

<!--TOP TWO BEDROOM-->
### <p align="center">Top Five Zip Codes for 2 Bedroom Homes</p>

Below are the top 5 zip codes for the 2 bedroom catagory. Again,'top' being defined as the zip codes having the highest sum of percentage increases from month to month over the last 18 years or so. Data for this catagory started in January of 2004.

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Vally Hi/North Laguna Neighborhoods (Sacramento City) </p>
<p align="center"><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95819 East Sacramento Neighborhood (Sacramento City) </p>
<p align="center"><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95824 Lemon Hill Neighborhood (Sacramento City) </p>
<p align="center"><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95834 Natomas Crossing Neighborhood (Sacramento City)</p>
<p align="center"><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City)</p>


<!--PERCENT DOLLAR FORECAST 5 FOR 2 BEDROOM-->
### <p align="center">Percent and Price Forecast for 2 Bedroom Homes in Top 5 Zip Codes</p>

None of the top 5 zip codes in the 2 bedroom home category are forecasted to see price increases through late 2025. <img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods in Sacramento which are projected to hold steady for pricing will be met by the <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95834 Natomas Crossing Neighborhood, also in the city of Sacramento, which historically had a higher price point (a, below).

<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> The 95824 Lemon Hill Neighborhood in the city of Sacramento will see percent decreases around the -1.25 to -1.4 range (b1. below) month over month. Lemon Hill, which historically had a higher average price point than <img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> the 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City) and <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway/Vally Hi/North Laguna Neighborhoods will drop below both those neighborhoods in average 2 bedroom home price. (b2. below)

<img width="994" alt="Screenshot (607) - Copy" src="https://user-images.githubusercontent.com/102890151/194685173-71c114ba-cdf7-4564-9efa-a4f39b2189c8.png">

[Back to Table of Contents](#forecasting-home-prices-in-sacramento-county-ca)
<br>

<!--THREE BEDROOM-->
## <p align="center">3 Bedroom Homes</p>

<!--TOP THREE BEDROOM-->
### <p align="center">Top Five Zip Codes for 3 Bedroom Homes,<p/>

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Vally Hi/North Laguna Neighborhoods (Sacramento City)</p>
<p align="center"><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95673 Rio Linda California  </p>
<p align="center"><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" />95834 Natomas Crossing Neighborhood (Sacramento City) </p>
<p align="center"><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City)</p>
<p align="center"><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95829 Vineyard Area (Elk Grove East)</p>


<!--PERCENT DOLLAR FORECAST TOP 5 FOR 3 BEDROOM-->
### <p align="center">Percent and Price Forecast for 3 Bedroom Homes in Top 5 Zip Codes</p>

Four of these zip codes almost move in unison (a. below) in the percent change from month to month forecast. The exception <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods will recover quicker from negative month to month decreases and move to 0% change (b1. below) resulting in little price change over the next few years. The 95815 Old North Sacramento/Cal Expo Neighborhoods is forecasted to surpass both <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway/Vally Hi/North Laguna Neighborhoods and <img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95673 Rio Linda in average 3 bedroom home price in 2025 (b2. below)

<img width="994" alt="Screenshot (610)" src="https://user-images.githubusercontent.com/102890151/194720134-4646cf83-f24d-4f84-bbb6-c9fd730c0545.png">





<!--4 BEDROOM-->
## <p align="center">4 Bedroom Homes</p>

<!--TOP 5 FOR 4 BEDROOM-->
### <p align="center">Top Five Zip Codes for 4 Bedroom Homes,<p/>

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> </p>
<p align="center"><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> </p>
<p align="center"><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> </p>
<p align="center"><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> </p>
<p align="center"><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> </p>

<!--PERCENT DOLLAR FORECAST TOP 5 FOR 4 BEDROOM-->
### <p align="center">Percent and Price Forecast for 4 Bedroom Homes in Top 5 Zip Codes</p>

<!--5 BEDROOM-->
## <p align="center">5 Bedroom Homes</p>

<!--TOP 5 FOR 5 BEDROOM-->
### <p align="center">Top Five Zip Codes for 5 Bedroom Homes,<p/>

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> </p>
<p align="center"><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> </p>
<p align="center"><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> </p>
<p align="center"><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> </p>
<p align="center"><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> </p>

<!--PERCENT DOLLAR FORECAST TOP 5 FOR 5 BEDROOM-->
### <p align="center">Percent and Price Forecast for 5 Bedroom Homes in Top 5 Zip Codes</p>

<!--MATHER/ANATOLIA BEDROOM-->
## <p align="center">Mather and Rancho Cordova CA</p>


<!--PERCENT DOLLAR FORECAST TOP 5 FOR MATHER/ANATOLIA BEDROOM-->
### <p align="center">Percent and Price Forecast for Mather CA</p>


<!--PERCENT DOLLAR FORECAST TOP 5 FOR MATHER/ANATOLIA BEDROOM-->
### <p align="center">Percent and Price Forecast for Anatolia Neighbohood (Rancho Cordova city </p>

<!--LINKS LINKS-->
### Links

 Jason Brownlee's, ['A Gentle Introduction to SARIMA for Time Series Forecasting in Python'](https://machinelearningmastery.com/sarima-for-time-series-forecasting-in-python/)


[back to top of page](#forecasting-home-prices-in-sacramento-county-ca)
