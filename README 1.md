## PRACTICAL 1 : TikTok

### Project Overview
This project involves building a basic TikTok-style web layout using Next.js with Tailwind CSS. The main goals include:

- Setting up a structured Next.js project
- Creating reusable layout and UI components
- Implementing core pages like profile, upload, explore, etc.
- Building a responsive video feed
- Adding login and registration functionality with form validation using `react-hook-form`

### Part 1: Getting Started

#### Step 1: Create Next.js App
```bash
npx create-next-app@latest
```
Use the following configuration: <br>
    TypeScript: ❌ <br>
    ESLint: ✅ <br>
    Tailwind CSS: ✅ <br>
    src/ directory: ✅ <br>
    App Router: ✅ <br>
    Import alias: ❌ <br>

```bash
npm install
npm run dev
```

#### Step 2: Clean the Project
Update src/app/page.js with a simple placeholder

Clean globals.css to retain only Tailwind directives:
```bash 
@tailwind base;
@tailwind components;
@tailwind utilities;
```

#### Step 3: Folder Structure
```
mkdir -p src/components/layout
mkdir -p src/components/ui
mkdir -p src/lib
mkdir -p src/app/profile
mkdir -p src/app/upload
```

#### Step 4: Create Layout Components
Create src/components/layout/MainLayout.jsx with basic layout and navigation.

#### Step 5: Modify Global Layout
Update src/app/layout.js to wrap pages in MainLayout.


### Part 2:  UI Development

#### Step 1: Install Icons
```bash 
npm install react-icons
```
#### Step 2: Sidebar & Navigation
Update MainLayout.jsx to include navigation to:
    Home
    Following
    Explore
    Live
    Profile
    Upload

#### Step 3: Video Components
Create VideoCard.jsx and VideoFeed.jsx in src/components/ui.

#### Step 4: Pages
Create or update the following files:
```
src/app/page.jsx
src/app/following/page.jsx
src/app/explore/page.jsx
src/app/live/page.jsx
src/app/upload/page.jsx
src/app/profile/page.jsx
```
Each should render dummy content or components as per layout needs.


### Part 3: Authentication with React Hook Form

#### Step 1: Install Package
```bash
npm install react-hook-form
```
#### Step 2: Login and Signup Pages
Create:
```
src/app/login/page.jsx
src/app/signup/page.jsx
```
Use react-hook-form with validations:
    Required fields
    Regex for email
    MinLength for password
    Match passwords on signup

#### Step 3: Navigation Integration
Update MainLayout.jsx to add login/signup buttons.

#### Step 4: Testing
Check for:
- Validation errors (missing fields, invalid formats)
- Password mismatch
- Loading states
- Successful form submissions