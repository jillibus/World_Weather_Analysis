World_Weather_Analysis
# World Weather Analysis

![logo](analysis/module6-logo.png)

## Overview
This project was to learn about how to utilize Application Programming Interfaces or API's.  Then we were to develop a small application, PlanMyTrip to see if we could find Cities, Hotels, Weather Details of the Cities, and plan a Trip and detail it on a Map.

## My Process
First I generated 2,000 random Latitudes and Longitudes, then submitted them via the Google Maps API and requested the information in JSON format if the Latitude and Longitude pairing returned a city.  

Reading the response from Google Maps, if we found a city, from these random parings, we retrieved the following information: City, Country, Latitude, Longitude, Maximum Temperature, Humidity, Cloudiness, Wind Speed and Current Description of each city, and stored it into a DataFrame.

![Clean Hotel](analysis/City_DF.png)

---
I then requested a user to enter their desired minimum temperature and maximum temperature of their perfect vacation.  I entered those values in our DataFrame as a filter and those cities that met the criteria, were saved into a new Dataframe for a 'perfect vacation'. My next task was go to back to Google Maps and look for the closest Hotel in each of those cities and added the new column, Hotel to the DataFrame.

![Vacation Dataframe](analysis/clean_hotel_df.png)

---
My next goal was to create a Vacation Itinerary.  I choose a city where we would depart from, three stops along the way, and we would return back to our originating city.  I chose these cities from our list of cities found in our Vacation Search.   With that chosen I then plotted a trip route showing our trip, creating details of our hotels with the markers on the map.

![route map](Vacation_Itinerary/WeatherPy_travel_map.png)





* _**Task:**_ Collect and analyze weather data across cities worldwide.
* _**Plan:**_ PlanMyTrip will use the data to recommend ideal hotels based on clients' weather preferences.
* _**Method:**_ Create a Pandas DataFrame with 500 or more of the world's unique cities and their weather data in real time. This process will entail collecting, analyzing, and visualizing the data.

Your analysis of the data will be split into three main parts, or stages.

### Resources
* Data Source: Google Maps API Connection
* Software: Python 3.7.10, Jupyter Notebook 6.3.0, CitiPy 0.0.5, APIs, JSON Traversals
 
## Collect the Data
* Use the NumPy module to generate more than 2,000 random latitudes and longitudes.
* Use the citipy module to list the nearest city to the latitudes and longitudes.
* Use the OpenWeatherMap API to request the current weather data from each unique city in your list.
* Parse the JSON data from the API request.
* Collect the following data from the JSON file and add it to a DataFrame:
1.  City, Country
2.  Latitude and longitude
3.  Maximum temperature
4.  Humidity
5.  Cloudiness
6.  Wind speed

## Exploratory Analysis with Visualization
* Create scatter plots of the weather data for the following comparisons:
1.  Latitude versus temperature
2.  Latitude versus humidity
3.  Latitude versus cloudiness
4.  Latitude versus wind speed
* Determine the correlations for the following weather data:
1.  Latitude versus temperature
2.  Latitude versus humidity
3.  Latitude versus cloudiness
4.  Latitude versus wind speed
* Create a series of heatmaps using the Google Maps and Places API that showcases the following:
1.  Latitude versus temperature
2.  Latitude versus humidity
3.  Latitude versus cloudiness
4.  Latitude versus wind speed

## Visualize Travel Data

* Create a heatmap with pop-up markers that can display information on specific cities based on a customer's travel preferences. Complete these steps:

1.  Filter the Pandas DataFrame based on user inputs for a minimum and maximum temperature.
2.  Create a heatmap for the new DataFrame.
3.  Find a hotel from the cities' coordinates using Google's Maps and Places API, and Search Nearby feature.
4.  Store the name of the first hotel in the DataFrame.
5.  Add pop-up markers to the heatmap that display information about the city, current maximum temperature, and a hotel in the city.
