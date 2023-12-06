## Introduction

Make a web app for users to see the current weather and the weather forecast for the next 7 days.

## Requirements

* Create a React app
* An input for users to type city name
* Display current weather including weather condition, temperature, humidity, wind speed, and date and time
* Visualization to display the temperature change, humidity change, and weather conditions of each day

The following image shows one way to implement the UI. Feel free to interpret the requirements however you'd like!
Weather forecast website project demo

![image](https://ucarecdn.com/6320962b-d4bf-4cfc-a66c-7972492f77c0/)

## Suggested Implementation

* Fetch user's device position. If you're unable to get the user's position, set London as the default location.
* Fetch weather data (forecast data and current weather data) of the location from weather API
* Format the data into charts
* Display the chart and current weather

## References

* [Create React app](https://github.com/facebook/create-react-app)
* [Getting device position](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation)
* [Chart.js](https://www.chartjs.org/): JavaScript charting
* [OpenWeather](https://openweathermap.org/) provides weather data APIs