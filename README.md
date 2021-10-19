# 2 Train Delays
A look at delays to the 2 Line<br>

As a proof of concept, I'm building a predictive model to determine what causes delays on the 2 line.<br>

If succesful, this model can be expanded to predict delays across all 26 lines in the New York City Subway System.<br>

I actually hope to do this for all lines after the program finishes, but I have to start somewhere.<br>

![image](https://user-images.githubusercontent.com/69225974/138002100-a41b741d-dfe3-4d53-87b2-d94faf743f1e.png)
<sup>Image courtesy of [Flickr](https://www.flickr.com/photos/55167823@N07/12951714935)<sub>


The business problem is straight forward. New Yorkers hate delays. The MTA/NYS Government would like to stop delays before they occur, as they
  are harmful to the city as a whole for a variety of reasons.<br>

My model took data from several sources to try and determine the main causes of delays on the IRT Line, the 2 Train:<br>
  * MTA Alerts Archive - an archive of all the delays across the NYC Subway System, stratified from Jan 01, 2010 through Sep 30, 2021<br>
  * NOAA Weather Data for NYC (JFK + Ctl Park)<br>
  * MTA Turnstile Data - inspecting the station usage<br>

I am also scouring for the following data, though I likely will wait until after my Capstone presentation for most of this:<br>
  * Planned service (there is planned service in the archive, but not much)<br>
  * Timestamped weather data (current data just has dates, I would love hourly reports)<br>
  * Although the MTA Financials [do exist](https://new.mta.info/transparency/financial-information/financial-and-budget-statements), I need
  a better way of going through it when I have more time to do so.<br>
  * Average train age for all active trains/lines<br>
  * Station and track damage (including tunnels)<br>
  
At my current stage, the data is cleaned with about 200 features to look through and model on.<br>
  
I have tested several models and plan to use an f1_score to determine my model success, as I'm testing 2 delays inside of all IRT train delays.<br>
  
I will be updating this ReadMe as I go and hopefully deploy an app soon enough!<br>
