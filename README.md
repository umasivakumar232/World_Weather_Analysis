# World Weather Analysis

## Project Overview

This project demonstrates our learning of using Application Programming Interfaces (APIs) to retrieve specific information regarding world weather and then using this weather information to help our client PlanMyTrip create specific travel itineraries using the Google Places and Maps APIs for their clients based on their specific holiday requirements.

## Resources

### Development Environment

* Anaconda – versions 4.10.3 
* Jupyter Notebook – version 6.10.0 
* Python – version 3.8.8

### Dependencies

* Python Pandas, Matplotlib, Numpy, Scipy Requests libraries
* CitiPy - A Python script to visualize data points of the weather for 500+ cities across the world of   varying distance from the equator. python jupyter-notebook pandas ...

### APIs

* OpenWeather API
* Google Places APIs
* Google Maps APIs
* Google Direction APIs 
  
## Project Details
This project can be divided into three parts  

### Weather Data 

In this part we generated 2000 random latitudes and longitudes, retrieved the nearest city based on the combination of latitudes and longitudes using the CitiPy module, and performed an API call with the OpenWeatherMap. We also used API skills to retrieve the current weather description for each city. Then, created a new DataFrame containing the updated weather data.

<img width="637" alt="Weather_Database" src="https://user-images.githubusercontent.com/85518330/126912068-2b492693-4627-41cf-a929-f658a7ad3f09.png">

 
### Vacation Search

In this part we used the

* Customer inputs to retrieve customer weather preferences, then we used those preferences to identify potential travel destinations and nearby hotels. 

<img width="712" alt="Customer_weather_preferences" src="https://user-images.githubusercontent.com/85518330/126912094-8724fafb-3c2f-4b61-b058-9b7739ae66b8.png">
 
* Basis our selection we  created a preferred_cities DataFrame. 

<img width="690" alt="Preferred_cities_df" src="https://user-images.githubusercontent.com/85518330/126912143-b779bf45-f0e0-4bfd-9f30-5bbb5551ab45.png">

* We added an empty column to our preferred_hotels DataFrame and named it Hotels_df 

<img width="438" alt="Adding_hotel_name" src="https://user-images.githubusercontent.com/85518330/126912204-fb6839fd-3c3a-40d1-97be-e8d72a28dc84.png">

* We used Google Maps and Places APIs to populate the hotel names column with the first hotel name from the results 

* We dropped all rows where the hotel name was missing to create a cleaned hotel_df 

<img width="532" alt="Hotels_df" src="https://user-images.githubusercontent.com/85518330/126912269-ddf6c6a1-7d9d-4bec-892c-eafb6cb64f84.png">

* Then, show those destinations on a marker layer map with pop-up markers

<img width="944" alt="WeatherPy_vacation_map" src="https://user-images.githubusercontent.com/85518330/126912237-cdfc9c8a-7b21-4b2e-bbba-a842628e2f01.png">


### Travel Itinerary

In this section we used the Google Directions API to create a travel itinerary that shows the route between four cities chosen from the customer’s possible travel destinations. Then, create a marker layer map with a pop-up marker for each city on the itinerary.

<img width="960" alt="WeatherPy_travel_map" src="https://user-images.githubusercontent.com/85518330/126913149-c61b05fd-b39c-45f4-a2a4-18ac390cf508.png">
<img width="960" alt="WeatherPy_travel_map_markers" src="https://user-images.githubusercontent.com/85518330/126913189-4ed49fe7-b7e9-46e8-b291-9bacdfa46db6.png">





