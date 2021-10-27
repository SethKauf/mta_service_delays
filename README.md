# MTA Service Delays on the IRT Line
A look at delays on the IRT Line<br>

For my final project at Flatiron, I analyzed the data on delays from the [MTA Alerts Archive](https://mymtaalerts.com/archive).<br>

I stratified this to Jan 01, 2010-Sep 30, 2021. Then by Agency to just NYCT Subway and no escelator/elevator information.<br>

I supplemented my analysis with:
* NYC Weather Data [from NOAA](https://www.ncdc.noaa.gov/cdo-web/datasets)<br>
* MTA Ridership Info from [MTA Website](https://new.mta.info/agency/new-york-city-transit/subway-bus-ridership-2020)<br>
* MTA Turnstile Info from [MTA Website](http://web.mta.info/developers/turnstile.html)<br>

![image](https://user-images.githubusercontent.com/69225974/138002100-a41b741d-dfe3-4d53-87b2-d94faf743f1e.png)
<sup>Image courtesy of [Flickr](https://www.flickr.com/photos/55167823@N07/12951714935)<sub>

The business problem is straight forward. New Yorkers hate delays. The MTA/NYS Government would like to stop delays before they occur, as they
  are harmful to the city as a whole for a variety of reasons.<br>

The NYT reported in 2017 that [delays cost $307 million annually](https://www.nytimes.com/2017/10/12/nyregion/subway-delays-lost-work-time-cost-new-york.html) in lost hours worked during the morning rush.<br>

As a proof of concept, I analyzed the delays to the IRT or Division A trains in the system. These are all the numbered lines and the 42nd street shuttle. [Here's more info on Wiki](https://en.wikipedia.org/wiki/A_Division_(New_York_City_Subway)).

<img src="images/Subway_map.PNG" width="600" height="500">
  <sup>Station locations on IRT line</sup><br>

  
To make my data useful, I did the following:<br>
  * Took out any "updates" so the same delay wouldn't be repeated<br>
  * Took out all planned service<br>
  * Took out station names for what station it was delayed at<br>
  * Took out all causes and turned them into features<br>
  * 
  * Created a "delayed_irt" column that was a 1 or 0 if the delay affected a train on the IRT line<br>
  * Feature engineered time and weather variables<br>
  * 
  

At my current stage, the data is cleaned with about 200 features to look through and model on.<br>
  
I have tested several models and plan to use an f1_score to determine my model success, as I'm testing 2 delays inside of all IRT train delays.<br>
  
I will be updating this ReadMe as I go and hopefully deploy an app soon enough!<br>
