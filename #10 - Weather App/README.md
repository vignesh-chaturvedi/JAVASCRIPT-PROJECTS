## NOTE:
You need to get your own api key from ([here](https://openweathermap.org/api)) and replace it in index.js file on line 8 :

```javascript
const APIKey = 'Your Api Key';
```
# Screenshot

![screenshot](ScreenShot.png)

### _Index.js Explanation_

This code snippet is responsible for fetching and displaying weather information based on the user's search input. Here's an explanation of the code:

1.  The `const` keyword is used to declare constant variables `container`, `search`, `weatherBox`, `weatherDetails`, and `error404`, and assigns them with corresponding elements retrieved from the DOM using `querySelector`.

2.  An event listener is added to the `search` element, which listens for a `'click'` event. When the event occurs (user clicks the search button), the callback function is executed.

3.  Inside the callback function, an API key and the value of the input field (`city`) are retrieved.

4.  If the `city` is empty, the function returns early and does not proceed with the API request.

5.  If the `city` is not empty, a `fetch` request is made to the OpenWeatherMap API, using the `city` value, API key, and desired units as parameters in the URL.

6.  The response from the API is handled using promises. The first `.then` method converts the response to JSON format.

7.  If the returned JSON object has a `cod` property equal to `'404'`, it means the city was not found. In this case, the error handling code is executed. It adjusts the styling and visibility of elements to show the "not found" error message.

8.  If the city is found (no '404' error), the error handling code is skipped. The weather information is extracted from the JSON object and assigned to corresponding elements in the DOM.

9.  Based on the weather condition (`json.weather[0].main`), the appropriate image source is set for the weather image element.

10. The temperature, description, humidity, and wind values are updated in their respective elements.

11. The display and visibility of weather-related elements are adjusted to show the weather information.

12. CSS classes are added to elements to trigger animations (`fadeIn`).

Overall, this code fetches weather information from the OpenWeatherMap API based on the user's search input, and updates the DOM elements accordingly to display the weather details.