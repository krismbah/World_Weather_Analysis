# World_Weather_Analysis

## Overview

The purpose of this analysis is to make changes recommended by the beta testers to the PlanMyTrip app. The following tasks are to be completed: 

1. Adding the weather description to the weather data you’ve already retrieved in this module.
2. Have the beta testers use input statements to filter the data for their weather preferences (Min temp = 60, Max temp = 90).
3. Identify potential travel destinations and nearby hotels.
4. From the list of potential travel destinations, have the beta testers choose four cities to create a travel itinerary.
5. Using the Google Maps Directions API, create a travel route between the four cities as well as a marker layer map.

## Results

***Deliverable 1: Retrieve Weather Data***
Generate a set of 2,000 random latitudes and longitudes, retrieve the nearest city, and perform an API call with the OpenWeatherMap. In addition to the city weather data gathered in this module, use API skills to retrieve the current weather description for each city. Then, create a new DataFrame containing the updated weather data.

Figure 1:

![City_Data_Df](https://raw.githubusercontent.com/krismbah/World_Weather_Analysis/main/Weather_Database/City_Data_Df.png)


***Deliverable 2: Create a Customer Travel Destinations Map***
Use input statements to retrieve customer weather preferences, then use those preferences to identify potential travel destinations and nearby hotels. Then, show those destinations on a marker layer map with pop-up markers.

Figure 2:

![Preferred_Cities_Df](https://raw.githubusercontent.com/krismbah/World_Weather_Analysis/main/Vacation_Search/Preferred_Cities.png)

Figure 3:

![WeatherPy_Vacation_Map](https://raw.githubusercontent.com/krismbah/World_Weather_Analysis/main/Vacation_Search/WeatherPy_vacation_map.png)


***Deliverable 3: Create a Travel Itinerary Map.***
Use the Google Directions API to create a travel itinerary that shows the route between four cities chosen from the customer’s possible travel destinations. Then, create a marker layer map with a pop-up marker for each city on the itinerary.

Figure 4:

![WeatherPy_Travel_Map](https://raw.githubusercontent.com/krismbah/World_Weather_Analysis/main/Vacation_Itinerary/WeatherPy_travel_map.png)

Figure 5:

![WeatherPy_Travel_Map_Markers](https://raw.githubusercontent.com/krismbah/World_Weather_Analysis/main/Vacation_Itinerary/WeatherPy_travel_map_markers.png)


## Summary

To summarize, the following were changes made to improve the PlanMyTrip app:

1. A set of 2000 random latitude and longitude cominations were generated and added to a list.
2. A request for Open Weather Map's API was run for each of those cities and data was parsed regarding max temperature, humidity, cloudiness, wind speed, country, and weather description.
3. 703 rows of data were generated and converted to a Pandas DataFrame. This dataframe then was used to create a csv file.
4. The csv file was imported and beta testers were prompted to chose a minimum and maximum location temperature of cities for vacation. The following cities were then created into a dataframe of preferred cities. The data was cleaned of rows with missing data.
5. A request for Google's API was run for each of those cities to search for hotels with 5000 meters.
6. The aforementioned process generated 414 cities. The data was created into a dataframe. Locations without a hotel name were removed.
7. The aforementioned dataframe was used to generate a csv.
8. A Google map with a marker layer was generated.
9. The aforementioned csv of vaction cities was then used to create a vaction dataframe.
10. Four cities from the map of the dataframe were picked to create a vacation itinerary route to travel between the four cities.
11. A direction layer map using the start and end latitude-longitude pairs. Mode of travel chosen was "Bicycling".
12. A marker layer map between the four cities was created and used to combine the four city DataFrames into one DataFrame with the concat() function.
13. Maps of the bicycling route between the four cities and a map of the region were created.
