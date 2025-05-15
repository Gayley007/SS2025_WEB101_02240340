## Practical 4 – Connecting TikTok Frontend to Backend

### Project Overview
This project extends the TikTok web frontend by integrating it with an Express.js backend. Key functionalities include:
- API client setup with authentication
- JWT-based login/logout
- Dynamic video feed from the backend
- User following, personalized feeds, and interactions (like, comment)
- Dynamic user profiles and discovery


### Project Setup

#### 1. Clone the Repositories

```bash
git clone https://github.com/syangche/TikTok_Frontend.git
git clone https://github.com/syangche/TikTok_Server.git
```
#### 2. Install Required Dependencies
```bash
npm install axios jwt-decode react-hot-toast react-hook-form
```

### Authentication

#### 1. API Configuration
Configured Axios in api-config.js with token interceptors.
JWT stored in localStorage.

#### 2. Auth Context
Implemented authContext.jsx to manage user state and token logic.
Wrapped app in AuthProvider inside layout.js.

#### 3. Auth UI
Built reusable modal (Modal.jsx)
Login/Register forms (AuthForms.jsx)
Integrated forms into modal (AuthModal.jsx)
Updated layout (MainLayout.jsx) with conditional login/logout UI


### Video Feed & Interaction
1. videoService.js
Functions for fetching, liking, and commenting on videos
2. VideoCard.jsx
Displays video info, like/comment buttons
Integrates real video data
3. VideoFeed.jsx
Handles fetching from API with loading/error states


### User Discovery & Following
Pages Created:
- /explore-users – discover and follow users
- /following – feed from followed users
- /profile/[userId] – dynamic user profile with videos

userService.js handles:
- Profile fetch
- Follow/unfollow actions


### Video Upload Page
- Upload form with fields for:
    - Video file
    - Caption
    - Thumbnail
- Authenticated upload only

