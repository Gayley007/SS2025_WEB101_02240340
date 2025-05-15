## PRACTICAL 2 : RESTful Weather API Web Application

### Project Overview
This project is a simple front-end application to interact with public REST APIs. It allows users to:
- Get real-time weather data via **GET** requests (OpenWeatherMap API)
- Save, update, and delete locations using **POST**, **PUT**, and **DELETE** requests (via JSONPlaceholder)

### Project Setup

1. Create a project folder and two files:
    index.html
    script.js

2. APIs used:
- **OpenWeatherMap API**: To fetch real-time weather data.
- **JSONPlaceholder API**: To simulate data persistence with POST, PUT, DELETE operations.

### HTML Structure (`index.html`)

The UI contains:
- Tab navigation for switching between actions
- Weather lookup form (GET)
- Location saving form (POST)
- Saved locations section (PUT & DELETE)
- Response display section
- Modal for editing locations

Key components:
- Input fields for city names and locations
- Buttons for each operation (Get, Save, Edit, Update, Delete)
- Areas to display API responses and feedback

### JavaScript Logic (`script.js`)

Features include:
- Event listeners for tab switching and form submission
- `getWeather()` — GET weather by city name
- `saveLocation()` — POST a location to JSONPlaceholder
- `editLocation()` — PUT to update a location
- `deleteLocation()` — DELETE a location
- DOM manipulation for UI updates
- Error handling and response display

### Usage Instructions

#### 1. API Key Setup
- Sign up at [OpenWeatherMap](https://openweathermap.org/) to get an API key.
- Replace the placeholder in your script:
```js
const apiKey = "YOUR_OPENWEATHERMAP_API_KEY";
```

#### 2. Run the App
- Open `index.html` in any web browser.
- No server setup required.

### Test Each API Feature

GET: Enter a city name and click "Get Weather". <br>
POST: Enter location details and click "Save Location".<br>
PUT: Click "Edit", update the info, and click "Update".<br>
DELETE: Click "Delete" next to a saved location.