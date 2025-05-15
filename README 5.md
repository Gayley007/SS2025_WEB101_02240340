## Practical 5 – Implementing Infinite Scroll with TanStack Query

### Project Overview
This practical implements **infinite scrolling** in the TikTok clone application using:

- **TanStack Query** (`useInfiniteQuery`) for state management
- **Cursor-based pagination** from the backend
- **Intersection Observer API** to detect scroll position

### Backend Setup (Express + Prisma)

#### Step 1: Update `getAllVideos` in `videoController.js`
- Replace `page` and `limit` with `cursor` and `limit`
- Return:
```js
{
  videos: [...],
  nextCursor: 'someVideoId',
  hasNextPage: true
}
```
#### Step 2: Update getFollowingVideos similarly
-Implements the same pagination approach for personalized feeds.<br>
**Tip**: Use Prisma’s cursor and skip with the n+1 pattern to check for more data.

### Frontend Implementation (Next.js)

#### Step 1: Install TanStack Query
```bash
npm install @tanstack/react-query @tanstack/react-query-devtools
```

#### Step 2: Setup QueryClientProvider
Wrap your app in src/app/layout.js:
```jsx
import { QueryClient, QueryClientProvider } from "@tanstack/react-query";
const queryClient = new QueryClient();

<QueryClientProvider client={queryClient}>
  {children}
</QueryClientProvider>
```

#### Step 3: Update videoService.js
Add a method that accepts a cursor parameter and fetches data accordingly

#### Step 4: Create Intersection Observer Hook
Create src/hooks/useIntersectionObserver.js to detect when a target element becomes visible.

#### Step 5: Update VideoFeed.jsx
- Use useInfiniteQuery instead of useQuery
- Use IntersectionObserver to trigger fetchNextPage()
- Append new pages to the existing video list

### Differences from Offset-Based Pagination
#### Backend:
- Uses cursor instead of page
- Returns nextCursor and hasNextPage
- Leverages efficient database lookups
#### Frontend:
- Switched to useInfiniteQuery
- Added Intersection Observer for smooth auto-loading
- No page numbers—rely on cursors only