## PRACTICAL 4: Connecting TikTok Frontend to Backend

### Key Concepts Applied

1. **API Client Configuration**
   - Set up a centralized Axios instance in `api-config.js` to handle requests to the backend.
   - Implemented request interceptors to attach JWT tokens to authenticated API calls.
   - Managed error responses globally for a cleaner user experience.

2. **JWT-Based Authentication**
   - Created `authContext.jsx` to manage authentication state across the app.
   - Used `localStorage` to store and retrieve JWT tokens.
   - Enabled login, signup, and logout functionality using modals and context.

3. **Dynamic UI Based on Auth State**
   - Used conditional rendering to show or hide navigation items depending on the login status.
   - Displayed user-specific data such as profile info and personalized feed.

4. **Real Video Feed Integration**
   - Fetched real video data from the backend instead of using mock data.
   - Updated `VideoFeed.jsx` and `VideoCard.jsx` to support like/unlike, comments, and playback.

5. **User Discovery and Following System**
   - Created `Explore Users` and `Following` pages using API calls.
   - Implemented follow/unfollow functionality and updated UI in real-time.
   - Supported dynamic user profiles and personalized video feeds.

6. **Upload and Protected Routes**
   - Allowed authenticated users to upload videos with captions and thumbnails.
   - Prevented access to protected pages (like upload) unless the user was logged in.


### What I Learned

- How to fully integrate a frontend (Next.js) with a backend (Express) using authenticated API calls.
- Managing global authentication state using React Context and JWT tokens.
- Connecting backend endpoints for videos, users, likes, and comments to a responsive UI.
- Building scalable React components that reflect real-time data interactions.
- Handling token-based security and cross-origin requests with proper configuration.


### Challenges Faced

#### 1. Invalid or Expired JWT Token
**Problem:** API requests failed due to expired or missing tokens  
**Solution:** Used `jwt-decode` to verify token expiration and redirected users to log in again.

#### 2. Incorrect Follow State Updates
**Problem:** Follow/unfollow UI did not reflect changes immediately  
**Solution:** Refetched user data or updated local state manually after follow actions.

#### 3. Comment and Like Delay
**Problem:** Like/unlike actions did not update until page refresh  
**Solution:** Used optimistic updates and revalidation techniques in service functions.

#### 4. CORS Errors Between Frontend and Backend
**Problem:** Cross-origin requests were being blocked  
**Solution:** Configured CORS middleware in the backend with allowed origins and credentials.

#### 5. Modal Not Closing After Login
**Problem:** AuthModal stayed open even after successful login  
**Solution:** Added a close function triggered by auth context state change.
