1. HTML Structure
The HTML file defines the structure of the Weather App. It includes:

A container for the app.

An input field for the user to enter a city name.

A button to trigger the weather search.

A div to display the weather information.

A div to show error messages.

Key HTML Elements:
<input type="text">: This is where the user enters the city name.

<button>: The "Get Weather" button triggers the API request.

<div id="weatherInfo">: This is where the weather data (temperature, humidity, etc.) is displayed.

<div id="errorMessage">: This is used to display error messages (e.g., if the city is not found).

2. CSS Styling
The CSS styles the app to make it visually appealing and user-friendly. It includes:

Centering the app on the page using flexbox.

Adding a card-like design with padding, borders, and shadows.

Styling the input field, button, and weather information for better readability.

Key CSS Features:
body: Centers the app vertically and horizontally using flexbox.

.container: Adds a white background, padding, rounded corners, and a shadow to create a card-like appearance.

input[type="text"]: Styles the input field with padding, borders, and rounded corners.

button: Styles the button with a blue background, white text, and rounded corners. It also changes color when hovered.

.weather-info: Styles the weather information section with proper spacing and alignment.

.error: Styles error messages in red for visibility.

3. JavaScript Functionality
The JavaScript code handles the app's logic, including:

Fetching weather data from the OpenWeatherMap API.

Displaying the weather data on the page.

Handling errors (e.g., invalid city names or API issues).

Adding interactivity (e.g., clicking the button or pressing Enter to search).

Key JavaScript Components:
a. Constants and Variables
apiKey: Stores the OpenWeatherMap API key (replace 'YOUR_API_KEY' with your actual key).

apiUrl: The base URL for the OpenWeatherMap API.

DOM Elements:

cityInput: The input field where the user enters the city name.

searchButton: The button to trigger the weather search.

weatherInfo: The div where weather data is displayed.

errorMessage: The div where error messages are displayed.

b. fetchWeather Function
This function fetches weather data from the API:

API Request:

Uses the fetch function to make a GET request to the OpenWeatherMap API.

The API URL includes the city name, API key, and units=metric to get temperature in Celsius.

Error Handling:

Checks if the response is OK (status code 200-299). If not, it throws an error.

Data Parsing:

Converts the API response to JSON.

Display Data:

Calls the displayWeather function to show the weather data.

Error Display:

If an error occurs (e.g., city not found), it displays an error message and clears the weather info.

c. displayWeather Function
This function formats and displays the weather data:

Destructuring:

Extracts relevant data from the API response (e.g., city name, temperature, weather description).

Weather Icon:

Constructs the URL for the weather icon using the icon code from the API.

HTML Template:

Creates a template string with the weather data and inserts it into the weatherInfo div.

d. Event Listeners
Button Click:

When the "Get Weather" button is clicked, it checks if the input field is not empty and calls the fetchWeather function.

Enter Key:

When the user presses the Enter key in the input field, it triggers the same functionality as the button click.

4. How the App Works
User Interaction:

The user enters a city name in the input field and clicks the "Get Weather" button or presses Enter.

API Request:

The app sends a request to the OpenWeatherMap API with the city name and API key.

Data Retrieval:

The API returns weather data for the specified city.

Data Display:

The app displays the weather data (city name, temperature, weather description, humidity, wind speed, and weather icon) in the weatherInfo div.

Error Handling:

If the city is not found or there is an API issue, an error message is displayed in the errorMessage div.

5. Key Features
Search by City: Users can enter any city name to get its current weather.

Weather Details:

Temperature (in Celsius).

Feels-like temperature.

Weather description (e.g., "clear sky").

Humidity and wind speed.

Weather icon (visual representation of the weather).

Error Handling:

Displays user-friendly error messages for invalid city names or API issues.

Responsive Design:

The app looks good on both desktop and mobile devices.
