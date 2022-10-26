<!--TITLE TITLE TITLE-->
# <p align="center">Forecasting Home Prices in Sacramento County CA<p/>

<!--OPENING IMAGE OPENING IMAGE-->
![Screenshot (466)](https://user-images.githubusercontent.com/102890151/187573030-680d3f0d-80cb-4081-8edd-9bd179ec3963.png)

<!--HIT COUNTER HIT HIT HIT-->
<img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FSringayKeno%2Fforecasting-home-prices-sacramento-county&count_bg=%23DCBB79&title_bg=%23555555&icon_color=%d2ae6c&title=page+visits&edge_flat=false" height="16" />&#160;&#160;<img src="https://img.shields.io/badge/made%20with-python-d2ae6c.svg" height="16" />

<!--TABLE OF CONTENTS TABLE TABLE-->
### <img src="https://via.placeholder.com/15/d2ae6c/d2ae6c.png" width="10" height="10" /> Table of Contents 
<details>
  <summary>Click to expand or hide</summary>
  
* [Analysis Overview](#analysis-overview)
* [Data Source](#data-source) 
* [Structure](#structure) 
* [Tech Stack](#tech-stack)
* [Method](#method)
   * [ARIMA and SARIMA In 45 Seconds](#arima-and-sarima-in-45-seconds)
   * [Why SARIMA](#why-sarima)
   * [Method-Top Five Zip Codes](#method-top-five-zip-codes)
* [Results](#results) 
   * [All Home Types](#all-home-types)
   * [Condos and Co-ops](#condos-and-co-ops)
   * [1 Bedroom Homes](#1-bedroom-homes)
   * [2 Bedroom Homes](#2-bedroom-homes)
   * [3 Bedroom Homes](#3-bedroom-homes)
   * [4 Bedroom Homes](#4-bedroom-homes)
   * [5 Bedroom Homes](#5-bedroom-homes)
   * [Rancho Cordova and Mather CA](#rancho-cordova-and-mather-ca)
      * [3 Bedroom Rancho Cordova and Mather CA](#3-bedroom-rancho-cordova-and-mather-ca)
      * [4 Bedroom Rancho Cordova and Mather CA](#4-bedroom-rancho-cordova-and-mather-ca)
      * [5 Bedroom Rancho Cordova and Mather CA](#5-bedroom-rancho-cordova-and-mather-ca)
         
* [Links](#links)

</details>

<!--Analysis OVERVIEW-->
## <p align="center">Analysis Overview<p/>


#### *This 8 part analysis is currently in progress thru Nov 2022. Using over 20 years of Zillow data, I identify the top 5 zip codes for home value in 7 different home catagories in Sacramento County California. Then, I forecast those homes values and percentage increases out for the next 3 years using the SARIMA forecasting model.*



<!--DATA SOURCE-->
<!--DATA SOURCE-->
##  <p align="center">Data Source<p/> 

Data was sourced from [Zillow Data's](https://www.zillow.com/research/data/) Home Value Index (ZHVI) category which is a smoothed, seasonally adjusted measure of the typical home value and market changes across a given region and housing type. It reflects the typical value for homes in the 35th to 65th percentile range.

<!--STRUCTURE-->
##  <p align="center">Structure<p/> 

   * [data_clean.ipynb](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/tree/main/data_cleaned) code for prepping and then subsetting data
   * [data_explored.ipynb](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/tree/main/data_explored) initial look at data and selection of top zip codes
   * [evaluation_of_model.ipynb](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/tree/main/evaluation_of_model) code to evaluate SARIMA model
   * [forecast.ipynb](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/tree/main/forecast) predicting! 

<!--TECH STACK-->
## <p align="center">Tech Stack<p/>

<p align="center">&#160;&#160;&#160;&#160;Software&#160;&#160;&#160;&#160;&#160;Language&#160;&#160;&#160;&#160;&#160;Markup&#160;&#160;&#160;Terminal&#160;&#160;Distribution<br> 
<img src="https://img.shields.io/badge/Jupyter-d2ae6c.svg?&style=for-the-badge&logo=Jupyter&logoColor=white" style="vertical-align:top; margin:3px" height="20" />&#160;&#160;&#160;&#160;<img src="https://img.shields.io/badge/Python-d2ae6c?style=for-the-badge&logo=python&logoColor=blue" style="vertical-align:top; margin:3px" height="20" />&#160;&#160;&#160;&#160;<img src="https://img.shields.io/badge/HTML5-d2ae6c?style=for-the-badge&logo=html5&logoColor=white" style="vertical-align:top; margin:3px" height="20" />&#160;&#160;&#160;&#160;<img src="https://img.shields.io/badge/GIT-d2ae6c?style=for-the-badge&logo=git&logoColor=white" style="vertical-align:top; margin:1px" height="20" />&#160;&#160;&#160;&#160;&#160;<img src="https://img.shields.io/badge/conda-d2ae6c.svg?&style=for-the-badge&logo=anaconda&logoColor=white" style="vertical-align:top; margin:3px" height="20" /><p/>                                                                                                                                                                                                                                                   <p align="center">&#160;Libraries 
<br><img src="https://img.shields.io/badge/Pandas-d2ae6c?style=for-the-badge&logo=pandas&logoColor=white" style="vertical-align:top; margin:3px" height="20" />&#160;&#160;<img src="https://img.shields.io/badge/numpy-d2ae6c.svg?style=for-the-badge&logo=numpy&logoColor=white" height="20" />&#160;&#160;<img src="https://img.shields.io/badge/matplotlib-d2ae6c.svg?style=for-the-badge&logo=matplotlib&logoColor=white" height="20" />&#160;&#160;<img src="https://img.shields.io/badge/seaborn-d2ae6c.svg?style=for-the-badge&logo=seaborn&logoColor=white" height="20" />&#160;&#160;<img src="https://img.shields.io/badge/pickle-d2ae6c.svg?style=for-the-badge&logo=pickle&logoColor=white" height="20" />&#160;&#160;<img src="https://img.shields.io/badge/statsmodel-d2ae6c.svg?style=for-the-badge&logo=statsmodel&logoColor=white" height="20" />&#160;&#160;<img src="https://img.shields.io/badge/sklearn-d2ae6c.svg?style=for-the-badge&logo=sklearn&logoColor=white" height="20" />&#160;&#160;<img src="https://img.shields.io/badge/math-d2ae6c.svg?style=for-the-badge&logo=math&logoColor=white" height="20" /><p/>                        
 
 
<!--METHOD-->
## <p align="center">Method<p/>


<!--ARIMA AND SARIMA In 60 Seconds-->
### <p align="center">ARIMA and SARIMA In 45 Seconds<p/>

If you are not familair with ARIMA/SARIMA models for forecasting, here's a quick glance to get you started and to gain an understanding about the method of forecasting used in this analysis.<br> <br>
ARIMA is an acronym for *'autoregressive integrated moving average'*. As the name suggests, this model involves three components: autoregressive, integrated and a third component, moving average. Those three components describe how ARIMA models the data. Each of these components are represented in the model as a parameter or trend element, usually as (p,d,q). In the model, the trend elements or parameters are replaced by integer values that dictate how much data is looked at (p, q) or how much the data is differenced (d). What integer values are used? They are determined through tests on the data. 

<p align="center"><img width="584" alt="Screenshot (741)" src="https://user-images.githubusercontent.com/102890151/197109152-3df28241-f3b9-434a-8e64-718459a921ed.png">
<p/>

##### <img align="right" width="250" height="210" alt="Screenshot (762)" src="https://user-images.githubusercontent.com/102890151/197448130-4a26b93d-0c4f-435f-9b39-da1c3b752862.png"><br><br><br>After the best integer values have been established (*image on right*) the model than can be defined (sarima= ...) the order is then set (order = ...) some rules are added (enforce_) than the model is fit (testing whether the model can explain the apparent forces at work in the observations) and then finally forecasted.
	

<br clear="right"/>
<br>	
SARIMA or '*seasonal autoregressive integrated moving average'*, is an ARIMA model that supports time series data with a seasonal component. Hence the 'S' for seasonal in front of ARIMA. SARIMA contains four additional elements that are not part of ARIMA; they are: P, D, Q and m. Like the elements for ARIMA, these four additional elements are also replaced by integer values that dictates how the data gets looked at.
<br><br>
	
For more information regarding SARIMA, I suggest a visit to Jason Brownlee's, ['A Gentle Introduction to SARIMA for Time Series Forecasting in Python'](https://machinelearningmastery.com/sarima-for-time-series-forecasting-in-python/) or Michelle Blumins, [A Simple Guide to Auto-ARIMA/SARIMA and Auto-ARIMAX/SARMAX](https://www.scmconnections.com/get-smart/simple-guide-auto-arima-sarima)

<!--WHY SARIMA WHY-->
### <p align="center">Why Sarima<p/>

After working with another algorithm, long short term memory (LSTM) for housing inventory predictions, which model didn't perform as well as I would have liked it too, I did further research. That research lead me to the SARIMA model, which proved to do well with data sets like the one I use for the project. The SARIMA model is suitable for time series data with trend and/or seasonal components, which I believed this data set contained.

<!--TOP 5 ZIP CODES-->	
### <p align="center">Method-Top Five Zip Codes<p/>
	
The Top zip codes were determined by looking at the difference from month to month in the price percentage increases over the period of data looked at. The period of data varied from home category to home catgory, but usually was in the range of 15-20 years. The zip codes with the highest sum of percentage increases are defined as top zip codes. Those top zip codes deviated furthest from the county average.
	
	
	
<p align="center"><img width="348" alt="Screenshot (764)" src="https://user-images.githubusercontent.com/102890151/197674468-a111e7a5-c6b3-4236-ab3a-98cab182f3c9.png"><p/>

 
<!--RESULTS-->
## <p align="center">Results<p/> 

<!--ALL TYPES-->
## <p align="center">All Home Types</p>

<!--ALL TYPES TOP 5-->
### <p align="center">Top Five Zip Codes for All Home Types<p/>

The top Five zip codes for this category, all home types are listed below. Again, the top zip codes were determined by looking at the difference from month to month in the price percentage increases over the last 20 years of data or 240 months. The zip codes with the highest sum of percentage increases are defined as top zip codes. The Sacramento County zip code for all home types closest to the average was 95632 which is Galt, a city in southern Sacramento County.

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Valley Hi/North Laguna Neighborhoods (Sacramento city)<br><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95630 Folsom California <br><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95834 Natomas Crossing Neighborhood (Sacramento city)<br> <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento city) <br><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95829 Vinyard (Elk Grove) </p>
	
	
##### <img align="right" width="250" height="210" src="https://user-images.githubusercontent.com/102890151/197659020-912e092f-6dc9-4fe1-9f9b-f6ada4e94871.jpg"><br><br><p align="center"> *(on right)* A home for sale in Folsom California (Autumn of 2022). Folsom, was second only to the Parkway and Valley Hi/North Laguna Neighborhoods (City of Sacramento) for percentage increases in the all home types catagory for Sacramento County.<br><br>


<!--PERCENT and Price FORECAST ALL HOME TYPES--><!--PERCENT and Price FORECAST ALL HOME TYPES--><!--PERCENT and Price FORECAST ALL HOME TYPES-->
### <p align="center">Percent and Price Forecast for All Home Types</p>

Looking over the results, it's interesting to note the zip code with the highest home average price <img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95630 Folsom California and the zip code with the lowest average home price of the top 5 zip codes <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods are the zip codes that will see the least decline. Both of those zip codes will hover near 0 percent (*a. below left*). 

<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> The Old North Sacramento/Cal Expo Neighborhoods will surpass <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> the Parkway and Valley Hi/North Laguna Neighborhoods in average home price (*b. below right*). Likewise <img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> the Natomas Crossing Neighborhood in Sacramento is forecasted to also meet the average home price of the <img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95829 Vinyard (Elk Grove) neighborhood (*c. below right*) which historically has been higher than the Natomas Crossing neighborhood.

<img width="994" alt="master_all_types - Copy" src="https://user-images.githubusercontent.com/102890151/196049933-2dfb00fc-2a8a-4c8a-8a54-2249b434a5ac.png">

<p align="center"><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95630 Folsom California &#160;<img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95829 Vinyard (Elk Grove) &#160;<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95834 Natomas Crossing Neighborhood (Sac city) <br><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Valley Hi/North Laguna Neighborhoods (Sacramento city) <br><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento city) </p> 

##### About This Data

<sup><sub>Data for All Home Types was sourced from [Zillow Data's](https://www.zillow.com/research/data/) Home Value Index (ZHVI) category. ZHIV is a smoothed, seasonally adjusted measure of the typical home value and market changes across a given housing type. It reflects the typical value for homes in the 35th to 65th percentile range.<sub><sup>
- <sup><sub>File name 'ZHIV All Home Types (SFR Condo/Co-op) Time Series, Smoothed, Seasonally Adjusted ($)'. File dated OCT 2022<sub><sup>
- <sup><sub>Data for analyis was from JAN 2003 - OCT 2022</sub></sup>
- <sup><sub>Data limitation. Zip codes 95742 and 95655 not in analysis (lack of data for those zip codes)<sub><sup>
- <sup><sub>Data code can be found here: [data_cleaned](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_cleaned_all_types.ipynb), [data_explored](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explored/data_explored_all_types.ipynb), [evaluation_of_model](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/evaluation_of_model/evaluated_model_all_types.ipynb) and [forecast](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/tree/main/forecast)<sub><sup>

[Back to Table of Contents](#forecasting-home-prices-in-sacramento-county-ca)
<br>
  
<!--CONDOS AND CO-OPS-->
## <p align="center">Condos and Co-ops</p>

<!--TOP 5 FOR FORECAST CONDOS-->
### <p align="center">Top Five Zip Codes for Condos and Co-ops</p>

The top Five zip codes for category Condos/Co-ops are listed below. Once again, the Top zip codes are determined by looking at the difference from month to month in the price percentage increase over the last 20 years of data. The zip codes with the highest sum of percentage increases are defined as top zip codes.

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Vally Hi/North Laguna Neighborhoods (Sacramento City)<br><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95630 Folsom California <br><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95811 Richards/part of Midtown/Southside Park Neighborhoods (Sacramento City) <br><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95814 Downtown Sacramento <br><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95841 Amber Park/Garfield Hills Area (N Highlands/Sacramento Cities)</p>

<!--PERCENT and Price FORECAST CONDOS--><!--PERCENT and Price FORECAST CONDOS--><!--PERCENT and Price FORECAST CONDOS-->
### <p align="center">Percent and Price Forecast for Condos and Coops</p>
 
<img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Valley Hi/North Laguna Neighborhoods will see monthly percent changes in the range of +.5 to +1.5 (*a1. below left*) causing the Parkway and Valley Hi/North Laguna averge one condo price to go above both that of <img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95841 Amber Park/Garfield Hills Area and <img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95630 Folsom California (*a2. below right*)

The two downtown Sacramento zips codes <img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95811 Richards/part of Midtown/Southside Park Neighborhoods and <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95814 Downtown Sacramento will fluctuate above and below 0 percent (*b1. below left*). <img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95811 will fluctuate between -1.25 and +1.25 almost evenly causing the one bedroom average price in that zip code to remain even in the forecast (*b2. below right*).

<img width="994" alt="Screenshot (683)" src="https://user-images.githubusercontent.com/102890151/196086251-51107b18-cfce-45ff-a396-1785a9ff9e1d.png">

<p align="center"><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95814 Downtown Sacramento &#160;<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95811 Richards/part of Midtown/Southside Park Neighborhoods <br><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95630 Folsom California &#160;<img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95841 Amber Park/Garfield Hills Area <br><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Vally Hi/North Laguna Neighborhoods</p>


##### About This Data
<sup><sub>Data for Condos and Coops was sourced from [Zillow Data's](https://www.zillow.com/research/data/) Home Value Index (ZHVI) category. ZHIV is a smoothed, seasonally adjusted measure of the typical home value and market changes across a given housing type. It reflects the typical value for homes in the 35th to 65th percentile range.<sub><sup>
- <sup><sub>File name 'ZHIV Condo/Coop Time Series ($). File dated OCT 2022<sub><sup>
- <sup><sub>Data for analyis was from JAN 2008 - OCT 2022</sub></sup>
- <sup><sub><sub>Data limitation. Zip codes 95827, 95818, and 95816 not in analysis (lack of data for those zip codes)<sup>
- <sup><sub>Data code can be found here: [data_cleaned](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_cleaned_condo.ipynb), [data_explored](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explored/data_explored_all_types.ipynb), [evaluation_of_model](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/evaluation_of_model/evaluated_model_condo.ipynb) and [forecast](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/forecast/forecast_condos.ipynb)<sub><sup>
  
[Back to Table of Contents](#forecasting-home-prices-in-sacramento-county-ca)
<br>

<!--ONE BEDROOM HOMES-->
## <p align="center">1 Bedroom Homes</p>

The amount of data for one bedrooms was limited to only 11 zip codes, most of which were located in the city of Sacramento. In this catagory, instead of looking at just the top 5 zip codes, all 11 zip codes will be examined.

<!--TOP 5 ONE BEDROOM-->
### <p align="center">Top Five Zip Codes for 1 Bedroom Homes</p>

Here are the top 5 zip codes for the 1 bedroom category. Again,'top' being defined as the zip codes having the highest sum of percentage increases from month to month over the last 10+ years or so. Data for this catagory started in March of 2009. Below are the top 5 zip codes.

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95628 Fair Oaks (City)<br><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95835 (north half) of North Natomas (Sacramento city)<br><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95833 South Natomas/Gardenland Neighborhoods (Sacramento city)<br><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95838 Robla, North Sacramento and Del Paso Heights Neighborhoods (Sacramento city)<br><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95820 Lawrence Park/Tahoe Park South Neighborhoods (Sacramento city)</p>


<!--PERCENT DOLLAR FORECAST 5 ONE BEDROOM-->
### <p align="center">Percent and Price Forecast for 1 Bedroom Homes</p>

Only one of the top five zip codes is forecasted to increase in price over the next few years. That zip code <img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95833 the South Natomas/Gardenland Neighborhoods, which is located adjacent to downtown will fluctuate between +.25 and +1.75 (*a1. below left*) in month to month percent increases. The price forecast (*a2. below right*) for 95833 looks much like it's historical past since 2014 as it continues to climb.

<img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> The 95628 zip code, Fair Oaks (City) is not going up or down, but rather is forecasted to flatline about at the 0% mark (*b1. below left*) resulting in little to no price changes at least until early 2026 (*b2. below right*). 

<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" />  95838 The Robla, North Sacramento and Del Paso Heights Neighborhoods, which are in the city of Sacramento will see month to month percent decreases around the -1.25 rate (*c1. below left*) and price reductions (*c2. below right*) that will take one bedrooms in that zip code back to 2018 values over the next few years.

The remaining two zip codes, all in the city of Sacramento <img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95835 (northern half) of North Natomas and <img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95820 Lawrence Park/Tahoe Park South Neighborhoods are all forecasted to see declines in price.


<img width="994" alt="Screenshot (718)" src="https://user-images.githubusercontent.com/102890151/196594663-aec4e7c2-8288-4e98-bcc7-34a0c75120c3.png">

  
<p align="center"><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95820 Lawrence Park/Tahoe Park South Neighborhoods (Sacramento city)<br><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95835 (north half) of North Natomas (Sacramento city) &#160;<img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95628 Fair Oaks (City)<br><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95833 South Natomas/Gardenland Neighborhoods (Sacramento city)<br><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95838 Robla, North Sacramento and Del Paso Heights Neighborhoods (Sacramento city)</p>


<!--ONE BEDROOM TWO DIRECTIONS A CLEAR PATTERN-->
### <p align="center">One Bedroom Two Directions (A Clear Pattern)</p>

	
Before looking at the last 6 remaining zip codes for the one bedroom category, let's take a look at all 11 of the one bedroom zip codes together. There was a clear delination in the home price forecast (image below). <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> Homes in downtown Sacramento and adjacent neighborhoods all forecasted increases. On the other hand one bedroom homes in <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> neighborhoods further away from downtown, which generally had a lower price point to their downtown area counterparts in the past, all forecasted decreases. <br/>


<p align="center"><img width="550" alt="Screenshot (714)" src="https://user-images.githubusercontent.com/102890151/196591238-1c0b9471-42f7-4c18-997e-535bf1e8f839.png"><p/>

<p align="center">&#8679;<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> Homes in Downtown Sacramento and adjacent neighborhoods<br>	
&#8681;<img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> Neighborhoods further from downtown <p/>

<!--PERCENT AND PRICE FORECAST 6 ONE BEDROOM-->
### <p align="center">Percent and Price Forecast for Remaining 6 Zip Codes in 1 Bedroom Home Catagory</p>

<p align="center">There were a total of 11 zip codes in the one bedroom category. Let's examine the remaining 6 (listed below).<p/>

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95825 Sierra Oaks/Arden Arcade<br>
<img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95815 Old North Sacramento<br>
<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95818 LandPark/Curtis Park<br>
<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95816 Midtown/East Sacramento Neighborhoods<br>
<img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95817 Oak Park/Fairgrounds<br>
<img src="https://via.placeholder.com/15/3AB227/3AB227.png" width="10" height="10" /> 95811 Richards/New Era Park/Southside Park<p/>
 
Five of the six remaining zip codes are adjacent to downtown Sacramento. Those zip codes are forecasted to fluctuate in the 0-1.5% increase range (*a1. below left*) resulting in steady price increases (*a2. below right*). The 6th zip code <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95825 Sierra Oaks/Arden Arcade, which is not adjacent to downtown, will see a steady -1.75% decline month to month (*b1. below left*) resulting in a forecasted price drop at least until late 2025 (*b2. below right*).

<img width="994" alt="Screenshot (707)" src="https://user-images.githubusercontent.com/102890151/196591887-5581aaef-8178-4e1e-8afd-7aa3cb0f15cc.png">


<p align="center"><img src="https://via.placeholder.com/15/3AB227/3AB227.png" width="10" height="10" /> 95811 Richards/New Era Park/Southside Park &#160;<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95816 Midtown/East Sacramento Neighborhoods <br><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95818 LandPark/Curtis Park &#160;<img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95817 Oak Park/Fairgrounds &#160;<img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95815 Old North Sacramento <br>
<img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95825 Sierra Oaks/Arden Arcade <p/>
  
##### About This Data
<sup><sub>Data for 1 Bedroom was sourced from [Zillow Data's](https://www.zillow.com/research/data/) Home Value Index (ZHVI) category. ZHIV is a smoothed, seasonally adjusted measure of the typical home value and market changes across a given housing type. It reflects the typical value for homes in the 35th to 65th percentile range.<sub><sup>
- <sup><sub>File name 'ZHIV 1 Bedroom Time Series ($)'. File dated OCT 2022<sub><sup>
- <sup><sub>Data for analyis was from MAR 2009 - OCT 2022</sub></sup>
- <sup><sub>Data was limited to 11 zip codes.<sub><sup>
- <sup><sub>Data code can be found here: [data_cleaned](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_cleaned_one_bedroom.ipynb), [data_explored](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explored/data_explored_one_bedroom.ipynb), [evaluation_of_model](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/evaluation_of_model/evaluated_model_one_bedroom%20.ipynb) and [forecast](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/forecast/forecast_one_bedroom.ipynb)<sub><sup>

[Back to Table of Contents](#forecasting-home-prices-in-sacramento-county-ca)
<br>

<!--TWO BEDROOM-->
## <p align="center">2 Bedroom Homes</p>

<!--TOP TWO BEDROOM-->
### <p align="center">Top Five Zip Codes for 2 Bedroom Homes</p>

Below are the top 5 zip codes for the 2 bedroom catagory. Again,'top' being defined as the zip codes having the highest sum of percentage increases from month to month over the last 18 years or so. Data for this catagory started in January of 2004.

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Vally Hi/North Laguna Neighborhoods (Sacramento City) <br><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95819 East Sacramento Neighborhood (Sacramento City) <br><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95824 Lemon Hill Neighborhood (Sacramento City) <br><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95834 Natomas Crossing Neighborhood (Sacramento City)<br><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City)</p>
	
<img align="right" width="240" height="200" src='https://user-images.githubusercontent.com/102890151/197842437-f6975ac4-f20e-46f4-8cd9-6299a5309ad1.jpg'>
	
##### <p align="right"><br> *(right)* A 2 bedroom home in East Sacramento<p><br>

<!--PERCENT DOLLAR FORECAST 5 FOR 2 BEDROOM-->
	
### <p align="center">Percent and Price Forecast for 2 Bedroom Homes</p>

None of the top 5 zip codes in the 2 bedroom home category are forecasted to see price increases through late 2025. <img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods in Sacramento which are projected to hold steady for pricing will be met by the <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95834 Natomas Crossing Neighborhood, also in the city of Sacramento, which historically had a higher price point (*a, below right*).

<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> The 95824 Lemon Hill Neighborhood in the city of Sacramento will see percent decreases around the -1.25 to -1.4 range (*b1. below left*) month over month. Lemon Hill, which historically had a higher average price point than <img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> the 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City) and <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway/Vally Hi/North Laguna Neighborhoods will drop below both those neighborhoods in average 2 bedroom home price. (*b2. below right*)


<img width="994" alt="Screenshot (726)" src="https://user-images.githubusercontent.com/102890151/196770553-170856dd-b077-43c5-a6da-50985cc660ba.png">


<p align="center"><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95819 East Sacramento Neighborhood  <br><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95834 Natomas Crossing Neighborhood &#160;<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95824 Lemon Hill Neighborhood <br><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods<br>&#160;<img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Vally Hi/North Laguna Neighborhoods</p>
  
##### About This Data
<sup><sub>Data for 2 Bedroom was sourced from [Zillow Data's](https://www.zillow.com/research/data/) Home Value Index (ZHVI) category. ZHIV is a smoothed, seasonally adjusted measure of the typical home value and market changes across a given housing type. It reflects the typical value for homes in the 35th to 65th percentile range.<sub><sup>
- <sup><sub>File name 'ZHIV 2 Bedroom Time Series ($)'. File dated OCT 2022<sub><sup>
- <sup><sub>Data for analyis was from JAN 2004 - OCT 2022</sub></sup>
- <sup><sub>Data limitation. Zip codes 95757,95832 not in analysis (lack of data for those zip codes)<sub><sup>
- <sup><sub>Data code can be found here: [data_cleaned](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_cleaned_two_bedroom.ipynb), [data_explored](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explored/data_explored_2bedroom.ipynb), [evaluation_of_model](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/evaluation_of_model/evaluated_model_two_bedroom.ipynb) and [forecast](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/forecast/forecast_two_bedroom.ipynb)<sub><sup>

[Back to Table of Contents](#forecasting-home-prices-in-sacramento-county-ca)
<br><br>

<!--THREE BEDROOM-->
## <p align="center">3 Bedroom Homes</p>

<!--TOP THREE BEDROOM-->
### <p align="center">Top Five Zip Codes for 3 Bedroom Homes,<p/>
	
Below are the top 5 zip codes for the 3 bedroom catagory. Again,'top' being defined as the zip codes having the highest sum of percentage increases from month to month over the last 18 years or so. Data for this catagory started in January of 2005.

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Vally Hi/North Laguna Neighborhoods (Sacramento City) <br><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95673 Rio Linda California  <br><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95834 Natomas Crossing Neighborhood (Sacramento City) <br><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City) <br><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95829 Vineyard Area (Elk Grove East)</p>
	
	
	
##### <img align="right" width="250" height="210" src=https://user-images.githubusercontent.com/102890151/197664214-7ecf14f0-a542-4f43-a25f-8a409527918d.jpg><br><p align="right"> *(on right)* A three bedroom home in zip code 95823 Parkway and Vally Hi/North Laguna Neighborhoods (Sacramento City)<br>


	
<!--PERCENT DOLLAR FORECAST TOP 5 FOR 3 BEDROOM-->
### <p align="center">Percent and Price Forecast for 3 Bedroom Homes</p>

Four of these zip codes almost move in unison (*a. below left*) in the percent change from month to month forecast. The exception <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods will recover quicker from negative month to month decreases and move to 0% change (*b1. below left*) resulting in little price change over the next few years. The 95815 Old North Sacramento/Cal Expo Neighborhoods is forecasted to surpass both <img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway/Vally Hi/North Laguna Neighborhoods and <img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95673 Rio Linda in average 3 bedroom home price in 2025 (*b2. below right*)

<img width="994" alt="Screenshot (734)" src="https://user-images.githubusercontent.com/102890151/196816475-6801de69-2d88-4bb7-8417-25cdbaaab660.png">

<p align="center"><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95829 Vineyard Area (Elk Grove East) &#160;<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95834 Natomas Crossing Neighborhood (Sacramento City) <br><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95673 Rio Linda California &#160;<img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Vally Hi/North Laguna Neighborhoods (Sacramento City) <br><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo Neighborhoods (Sacramento City)</p>
  
 ##### About This Data
<sup><sub>Data for 3 Bedroom was sourced from [Zillow Data's](https://www.zillow.com/research/data/) Home Value Index (ZHVI) category. ZHIV is a smoothed, seasonally adjusted measure of the typical home value and market changes across a given housing type. It reflects the typical value for homes in the 35th to 65th percentile range.<sub><sup>
- <sup><sub>File name 'ZHIV 3 Bedroom Time Series ($)'. File dated OCT 2022<sub><sup>
- <sup><sub>Data for analyis was from JAN 2005 - OCT 2022</sub></sup>
- <sup><sub>Data limitation. Zip codes 95830 and 95742 not in analysis (lack of data for those zip codes)<sub><sup>
- <sup><sub>Data code can be found here: [data_cleaned](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_cleaned_three_bedroom.ipynb), [data_explored](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explored/data_explored_three_bedroom%20.ipynb), [evaluation_of_model](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/evaluation_of_model/evaluated_model_three_bedroom.ipynb) and [forecast](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/forecast/forecast_three_bedroom.ipynb)<sub><sup>
	
[Back to Table of Contents](#forecasting-home-prices-in-sacramento-county-ca)
<br>


<!--4 BEDROOM-->
## <p align="center">4 Bedroom Homes</p>

<!--TOP 5 FOR 4 BEDROOM-->
### <p align="center">Top Five Zip Codes for 4 Bedroom Homes,<p/>
	
Below are the top 5 zip codes for the 4 bedroom catagory. Again,'top' being defined as the zip codes having the highest sum of percentage increases from month to month over the last 18 years or so. Data for this catagory started in January of 2008.

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Valley Hi/North Laguna (Sacramento city) <br><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95816 Marshall School/Newton Booth (Sacramento city) <br><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95824 95824 Lemon Hill/Cloverdale Manor (Sacramento city) <br> <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95834 Natomas Crossing (Sacramento city) <br> <img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo (Sacramento city) </p>

<!--PERCENT DOLLAR FORECAST TOP 5 FOR 4 BEDROOM-->
### <p align="center">Percent and Price Forecast for 4 Bedroom Homes</p><br>


<img width="488" alt="Screenshot (621)" src="https://user-images.githubusercontent.com/102890151/195249356-e6d5bfd0-8d64-4b8e-87e5-264ba606d0b1.png">&#160;<img width="488" alt="Screenshot (622)" src="https://user-images.githubusercontent.com/102890151/195249367-543e4a8c-23ef-4952-ae01-d6db3d932200.png">


<p align="center"><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95816 Marshall School/Newton Booth (Sacramento city) &#160; <img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95834 Natomas Crossing (Sacramento city) <br><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Valley Hi/North Laguna (Sacramento city) <br><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95815 Old North Sacramento/Cal Expo (Sacramento city) <br><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95824 Lemon Hill/Cloverdale Manor (Sacramento city) <br> </p>

  
##### About This Data
<sup><sub>Data for 4 Bedroom was sourced from [Zillow Data's](https://www.zillow.com/research/data/) Home Value Index (ZHVI) category. ZHIV is a smoothed, seasonally adjusted measure of the typical home value and market changes across a given housing type. It reflects the typical value for homes in the 35th to 65th percentile range.<sub><sup>
- <sup><sub>File name 'ZHIV 4 Bedroom Time Series ($)'. File dated OCT 2022<sub><sup>
- <sup><sub>Data for analyis was from JAN 2008 - OCT 2022</sub></sup>
- <sup><sub>Data limitation. Zip code 95830 not in analysis (lack of data for those zip codes)<sub><sup>
- <sup><sub>Data code can be found here: [data_cleaned](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_cleaned_four_bedroom.ipynb), [data_explored](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explored/data_explored_four_bedroom.ipynb), [evaluation_of_model](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/evaluation_of_model/evaluated_model_four_bedroom.ipynb) and [forecast](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/forecast/forecast_4bedroom%20.ipynb)<sub><sup>
	
[Back to Table of Contents](#forecasting-home-prices-in-sacramento-county-ca)
<br>

<!--5 BEDROOM-->
## <p align="center">5 Bedroom Homes</p>

<!--TOP 5 FOR 5 BEDROOM-->
### <p align="center">Top Five Zip Codes for 5 Bedroom Homes,<p/>
	
Below are the top 5 zip codes for the 5 bedroom catagory. Again,'top' being defined as the zip codes having the highest sum of percentage increases from month to month over the last 18 years or so. Data for this catagory started in January of 2008.

<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Valley Hi/North Laguna (Sacramento city) <br><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95820 North City Farms/Tahoe Park South (Sacramento city) <br><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95660 North Highlands Ca <br><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95662 Orangevale Ca <br><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95824 Lemon Hill/Cloverdale Manor (Sacramento city) <p/>

<!--PERCENT DOLLAR FORECAST TOP 5 FOR 5 BEDROOM-->
### <p align="center">Percent and Price Forecast for 5 Bedroom Homes</p><br>

<img width="450" alt="Screenshot (620)" src="https://user-images.githubusercontent.com/102890151/195220291-81053013-587d-4734-9683-3204fddeb6d7.png">&#160;<img width="523" alt="Screenshot (619)" src="https://user-images.githubusercontent.com/102890151/195220300-128ca2fa-3cc0-4ea3-bc2f-7bb5e99e299e.png">

<p align="center"><img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95662 Orangevale Ca &#160;<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95660 North Highlands Ca <br><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95823 Parkway and Valley Hi/North Laguna (Sacramento city) <br><img src="https://via.placeholder.com/15/A569BD/A569BD.png" width="10" height="10" /> 95824 Lemon Hill/Cloverdale Manor (Sacramento city)<br><img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" /> 95820 North City Farms/Tahoe Park South (Sacramento city) <p/>


  
##### About This Data
<sup><sub>Data for 5+ Bedroom was sourced from [Zillow Data's](https://www.zillow.com/research/data/) Home Value Index (ZHVI) category. ZHIV is a smoothed, seasonally adjusted measure of the typical home value and market changes across a given housing type. It reflects the typical value for homes in the 35th to 65th percentile range.<sub><sup>
- <sup><sub>File name 'ZHIV 5+ Bedroom Time Series ($)'. File dated OCT 2022<sub><sup>
- <sup><sub>Data for analyis was from FEB 2007 - OCT 2022</sub></sup> 
- <sup><sub>Data limitation. Zip codes 95842, 95832 and 95742 not in analysis (lack of data for those zip codes)<sub><sup>
- <sup><sub>Data code can be found here: [data_cleaned](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_cleaned_five_bedroom.ipynb), [data_explored](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explored/data_explored_five_bedroom.ipynb), [evaluation_of_model](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/evaluation_of_model/evaluated_model_five_bedroom.ipynb) and [forecast](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/forecast/forecast_five_bedroom.ipynb)<sub><sup>
	
[Back to Table of Contents](#forecasting-home-prices-in-sacramento-county-ca)
<br>

<!--RANCHO CORDOVA AND MATHER-->
## <p align="center">Rancho Cordova and Mather CA</p>



  
<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95670 Gold River CA and Cordova Court/Villages of Zinfindel (Rancho Cordova city) <br>
<img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95827 Bradshaw Woods/Jordan Estates (Rancho Cordova city)<br>
<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95742 Anatolia (Rancho Cordova city) <br>
<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95655 Mather CA<br>

### <p align="center">3 Bedroom Rancho Cordova and Mather CA</p>
  

<img width="480" alt="Screenshot (536)" src="https://user-images.githubusercontent.com/102890151/195751378-3a17f89f-1c86-4c37-90e6-95c3c48b8465.png">&#160;<img width="495" alt="Screenshot (537)" src="https://user-images.githubusercontent.com/102890151/195751390-ab0782e2-bd82-4071-9089-c8a3e6a59273.png">
	
<p align="center"><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95742 Anatolia (Rancho Cordova city) &#160;<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95655 Mather CA<br><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95670 Gold River CA and Cordova Court/Villages of Zinfindel (Rancho Cordova city) <br>
<img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95827 Bradshaw Woods/Jordan Estates (Rancho Cordova city)<p/>


### <p align="center">4 Bedroom Rancho Cordova and Mather CA</p>
  
<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95670 &#160;<img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95827 &#160;<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95742 &#160;<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95655 Mather CA <br>

<img width="480" alt="Screenshot (534)" src="https://user-images.githubusercontent.com/102890151/195751395-40f8f83e-074f-43e1-ab1a-322305481a93.png">&#160;<img width="497" alt="Screenshot (535)" src="https://user-images.githubusercontent.com/102890151/195751409-78ed1685-de99-4385-b3d6-27147de484b0.png">

<p align="center"><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95742 Anatolia (Rancho Cordova city) &#160;<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95655 Mather CA<br><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95670 Gold River CA and Cordova Court/Villages of Zinfindel (Rancho Cordova city) <br>
<img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95827 Bradshaw Woods/Jordan Estates (Rancho Cordova city)<p/>
	


### <p align="center">5 Bedroom Rancho Cordova and Mather CA</p>
  
<p align="center"><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95670 &#160;<img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95827 &#160;<img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95742 &#160;<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95655 Mather CA <br>
  
<img width="480" alt="Screenshot (532)" src="https://user-images.githubusercontent.com/102890151/195751419-65721a26-dc3a-4291-8b38-a9a69a3419fa.png">&#160;<img width="490" alt="Screenshot (533)" src="https://user-images.githubusercontent.com/102890151/195751432-7037c686-219a-4fff-a372-c710bc449bf6.png">

<p align="center"><img src="https://via.placeholder.com/15/99751b/99751b.png" width="10" height="10" /> 95742 Anatolia (Rancho Cordova city) &#160;<img src="https://via.placeholder.com/15/D8D051/D8D051.png" width="10" height="10" /> 95655 Mather CA<br><img src="https://via.placeholder.com/15/2E86C1/2E86C1.png" width="10" height="10" /> 95670 Gold River CA and Cordova Court/Villages of Zinfindel (Rancho Cordova city) <br>
<img src="https://via.placeholder.com/15/40E0D0/40E0D0.png" width="10" height="10" />  95827 Bradshaw Woods/Jordan Estates (Rancho Cordova city)<p/>



##### About This Data
<sup><sub>Data for Rancho Cordova and Mather CA was sourced from [Zillow Data's](https://www.zillow.com/research/data/) Home Value Index (ZHVI) category. ZHIV is a smoothed, seasonally adjusted measure of the typical home value and market changes across a given housing type. It reflects the typical value for homes in the 35th to 65th percentile range.<sub><sup>
- <sup><sub>File used:<sub><sup>
     * <sup><sub>'ZHIV 3 Bedroom Time Series ($)'. File dated OCT 2022<sub><sup>
     * <sup><sub>'ZHIV 4 Bedroom Time Series ($)'. File dated OCT 2022<sub><sup>
     * <sup><sub> and 'ZHIV 5 Bedroom Time Series ($)'. File dated OCT 2022<sub><sup>
- <sup><sub>Data for analysis was from  JAN 2010 - OCT 2022 for Rancho Cordova 3 Bedroom, FEB 2006 - OCT 2022 for Rancho Cordova 4 Bedroom, and JAN 2010 - OCT 2022 for Rancho Cordova 5 Bedroom</sub></sup> 
- <sup><sub>Data limitation. Zip code 5741 not in analysis (there was no data for that zip code)<sub><sup>
- <sup><sub>Data code can be found here:<sub><sup>
	
  * <sup><sub>for Rancho Cordova 3 Bedroom: [data_cleaned](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_cleaned_rancho_cordova_3_bedroom.ipynb), [data_explored](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explored/data_explored_rancho_cordova_three_bedroom.ipynb), [evaluation_of_model](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/evaluation_of_model/evaluated_model_rancho_three_bedroom.ipynb) and [forecast](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/forecast/forecast_rancho_three_bedroom.ipynb)<sub><sup>
	
  * <sup><sub>Rancho Cordova 4 Bedroom: [data_cleaned](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_cleaned_rancho_cordova_four_bedroom%20.ipynb), [data_explored](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explored/data_explored_rancho_cordova_four_bedroom.ipynb), [evaluation_of_model](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/evaluation_of_model/evaluated_model_rancho_four_bedroom.ipynb) and [forecast](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/forecast/forecast_rancho_four_bedroom.ipynb)<sub><sup>
	
  * <sup><sub>and Rancho Cordova 5 Bedroom: [data_cleaned](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_cleaned/data_cleaned_rancho_cordova_five_bedroom.ipynb), [data_explored](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/data_explored/data_explored_rancho_cordova_five_bedroom%20.ipynb), [evaluation_of_model](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/evaluation_of_model/evaluated_model_rancho_five_bedroom.ipynb) and [forecast](https://github.com/SringayKeno/forecasting-home-prices-sacramento-county/blob/main/forecast/forecast_rancho_five_bedroom.ipynb)<sub><sup>

<!--LINKS LINKS-->
### Links

 Jason Brownlee's, ['A Gentle Introduction to SARIMA for Time Series Forecasting in Python'](https://machinelearningmastery.com/sarima-for-time-series-forecasting-in-python/)
	
Michelle Blumins, [A Simple Guide to Auto-ARIMA/SARIMA and Auto-ARIMAX/SARMAX](https://www.scmconnections.com/get-smart/simple-guide-auto-arima-sarima)
	

Data was sourced from [Zillow.com research and data page](https://www.zillow.com/research/data/)


[Back to top of page](#forecasting-home-prices-in-sacramento-county-ca)
