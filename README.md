# Weather Api
This is an API built using ASP.NET Core that uses the OpenWeatherMap API.

Contains no view. Please use the React App in the weatherweb repo https://github.com/MartynFung/weatherweb.

# Setup
- Clone this repo
- NOTE: the OpenWeatherApi key has not been included in this repo. Please sign up for an account at https://home.openweathermap.org/users/sign_up to obtain an API key. It may take a few hours before the key becomes active. 
Enter in the key under WeatherApiCore > Controllers > WeatherController.cs at "string apiKey = _____"
- Clone the front-end React Client: https://github.com/MartynFung/weatherweb
- Open weatherapi with Visual studio 2017 > run with IIS Express
- Open weatherweb with VSCode > open console using CTRL+` > npm start
```
npm start
```
# OpenWeatherApi
- https://openweathermap.org/
- Example: http://api.openweathermap.org/data/2.5/weather?zip=92612,us&appid=ENTER_API_KEY_HERE

# Usage
- With the API and React Client running, enter in a valid US zipcode and click the "Get Weather" button


# Features
- Takes in a US Zipcode as input
- Displays weather for the provided zipcode including: City, Country, Temp, Temp_max, Temp_min, Description
- Caches forecast details in sessionStorage
- Subsequent requests for cached zipcodes (within 30 minutes of last API call) will be pulled from the cache to display weather.
- There is an indicator stating whether the current weather was pulled from the cache or not.
