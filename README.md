# Weather and Vacation Location Data Analysis 
By Kiana Navarre

**Programming Language Used: Python/API**

## Description
This repository is devided into 2 sections: WeatherPy and VacationPy.  For both sections, API keys are used to pull data from online databases.  In the WeatherPy file, data is pulled from OpenWeatherMap.org. In the VacationPy file, data is pulled from Geoapify.com. 

## Pre-requisite to Run Scripts 
To run this script, you will need your own API Key for OpenWeatherMap and Geoapify. 
1. Obtain API keys from OpenWeatherMap and Geoapify sites. 
    
      *Note: In order to obtain an API key from OpenWeatherMap you may need to input your credit card information. 
    
     *Reminder: Be sure to check API call usage prior to running/editing the scripts! 
2. Prior to running either the VacationPY.ipynb or the WeatherPy.ipynb file, add your API Keys as string values to the "api_keys.py" file in the WeatherPy folder. The formatting of this file should match:

    #OpenWeatherMap API Key
    weather_api_key = "insert_your_api_key_here"

    #Geoapify API Key
    geoapify_key = "insert_your_api_key_here"
3. Save the api_keys.py file

## WeatherPy
In this section, OpenWeatherMap.org is used to pull the weather information for a list of cities randomly generated from a latitude range of -90 to 90 and an longitude range of -100 to 100 using the citipy library. In order to analyze this data, the following scatter plots and linear regression plots were created. 

 ### Scatter Plots: 
 - City Latitude vs. Max Temperature (2023-01-23)
 - City Latitude vs. Humidity (2023-01-23)
 - City Latitude vs. Cloudiness (2023-01-23)
 - City Latitude vs. Wind Speed (2023-01-23)
 ### Linear Regression Plots:
- Northern Hemisphere: City Latitude vs. Max Temperature
- Southern Hemisphere: City Latitude vs. Max Temperature
- Northern Hemisphere: City Latitude vs. Humidity
- Southern Hemisphere: City Latitude vs. Humidity
- Northern Hemisphere: City Latitude vs. Cloudiness
- Southern Hemisphere: City Latitude vs. Cloudiness
- Northern Hemisphere: City Latitude vs. Wind Speed
- Southern Hemisphere: City Latitude vs. Wind Speed

## VacationPy
In this section, hvplot is used to generate a map plotting citiy points on a world map with the size of the points correlating to the humidity for each city.  The city information is pulled from the cities.csv file in the "output_data" folder.  Next, the cities data frame is narrowed down to only include weather conditions correlating to: 
- Temperature between 10°C and 27°C
- Clear Skies (No  Cloudiness)
- Humidity levels between 30% and 50%
- Wind Speed less than 8m/s

In the following steps, geoapify.com is used to pull hotel information correlating to the cities matching the above weather conditions.  These hotels are then plotted on a world map with the hotel name and country information available in a hover message for each city.  