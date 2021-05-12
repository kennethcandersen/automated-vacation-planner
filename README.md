# AUTOMATED WEATHER ANALYSIS & VACATION PLANNER
<img width="958" alt="AUTOMATED WEATHER ANALYSIS & VACATION PLANNER" src="https://github.com/kennethcandersen/automated-vacation-planner/blob/main/VacationPy/screenshot_heatmap.png">

### EXECUTIVE SUMMARY & OBJECTIVE

A program that automatically generates a list of ideal weather vacation spots based on real-time climate conditions specified by the user, locates and plots the best hotel recommendations provided my Google Maps API. Also analyzes the correlation between latitude and various weather conditions. 

### REPOSITORY NAVIGATION

- [*The WeatherPy folder*](https://github.com/kennethcandersen/automated-vacation-planner/tree/main/WeatherPy) contains code to select 500+ random cities, retrieve real-time weather data for those cities using the OpenWeather API, and automatically plots the correlation between latitude and temperature, humidity, cloudiness and windspeed. 
- [*The VacationPy*](https://github.com/kennethcandersen/automated-vacation-planner/tree/main/VacationPy) folder contains code that filters the 500+ cities for the ideal vacation location based on specified climate conditions, then plots a heatmap with hotel recommendations from the Google Maps API. 

### DATA
- [*OpenWeather*](https://openweathermap.org/) API for weather data
- [*Google Maps API*](https://developers.google.com/maps) for heatmap plotting, hotel search and hotel locations
- [*Citipy*](https://pypi.org/project/citipy/) for data on city locations

### TECHNOLOGIES
- Python
- Pandas in Juypyter Notebook
- Matploblib

### DEPENDENCIES

from datetime import datetime
from scipy import stats
import random
from citipy import citipy 
import matplotlib.pyplot
import pandas
import numpy
import requests, json, re
import gmaps
import os

### DATA EXPLORATION & CLEANUP

- Generate 1000 random latitude and longitude coordinates
- Use Citipy to find closest city to each set of coordinates
- Use OpenWeather API to retrieve real-time weather data on each city and create a pandas dataframe
- Backup data to csv file
- Drop cities with missing weather data, leaving 500+ cities to analyze and plot

### DATA ANALYSIS

- Plot correlation between latitude of the 500+ cities and weather conditions. Results:
<img width="958" alt="Latitude vs Weather Conditions" src="https://github.com/kennethcandersen/automated-vacation-planner/blob/main/WeatherPy/output_data/weather-conditions-vs-latitude.jpg">

- Plot correlation between latitude and weather conditions, by hemisphere. Results:
<img width="958" alt="Latitude vs Weather Conditions by Hemisphere" src="https://github.com/kennethcandersen/automated-vacation-planner/blob/main/WeatherPy/output_data/weather-conditions-vs-latitude-by-hemisphere.jpg">

- Plot humidity levels with a heatmap. Results:

### DATA TRANSFORMATION
- Filter climate data for ideal vacation locations based on specific climate conditions
- Use Google Map API to find hotel names and locations, and plot them on the heatmap. Results:
<img width="958" alt="Ideal Vacation Planner Example" src="https://github.com/kennethcandersen/automated-vacation-planner/blob/main/VacationPy/screenshot_heatmap2.png">


