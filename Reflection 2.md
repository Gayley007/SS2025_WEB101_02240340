## PRACTICAL 2 : Weather API Application 
### Key Concepts Applied

1. **RESTful API Operations**
   - GET: Used OpenWeatherMap to fetch weather data by city
   - POST/PUT/DELETE: Used JSONPlaceholder to simulate saving and managing user-entered locations

2. **JavaScript DOM Manipulation**
   - Dynamic UI updates based on API responses
   - Modals and form handling for editing and deleting locations

3. **Asynchronous Programming**
   - Used `fetch()` with async/await for API requests
   - Handled loading states and errors gracefully


### What I Learned

- How to perform real-world API interactions using JavaScript
- Practical usage of HTTP methods (GET, POST, PUT, DELETE)
- How to manage dynamic HTML content based on user input and API results
- Working with API keys securely and responsibly


### Challenges & Solutions

#### 1. API Key Issue
**Problem:** Forgot to replace the placeholder `YOUR_OPENWEATHERMAP_API_KEY`  
**Solution:** Generated a free key at [openweathermap.org](https://openweathermap.org) and updated the code.

#### 2. JSONPlaceholder Limits
**Problem:** No actual data persistence with JSONPlaceholder  
**Solution:** Treated it as a mock API and added clear explanations in UI that data is not actually saved.

#### 3. CORS Errors in Some Browsers
**Problem:** CORS errors when testing DELETE requests  
**Solution:** Ensured all requests were made with correct headers and used localhost only.
