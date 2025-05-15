## PRACTICAL 5: Infinite Scroll

### Key Concepts Applied
1. **Cursor-Based Pagination**
   - More stable and efficient than offset pagination
   - Implemented in both global and following video feeds

2. **TanStack Query (`useInfiniteQuery`)**
   - Automatically handles pagination state and data caching
   - Supports loading additional pages on-demand

3. **Intersection Observer**
   - Efficient detection of scroll-to-bottom
   - Replaces traditional scroll event listeners for better performance

4. **Prisma Cursor Pagination**
   - Backend optimized with `cursor`, `skip`, `take`, and `orderBy` for scalable queries


### What I Learned
- How infinite scroll improves UX by reducing manual pagination
- Replacing offset pagination with cursor-based pagination using Prisma
- Setting up `useInfiniteQuery` for frontend pagination
- Efficient scroll detection using the Intersection Observer API
- Integrating backend data streams smoothly into UI rendering


### Challenges Faced

#### 1. useInfiniteQuery Not Fetching More Pages
**Problem:** `fetchNextPage()` wasn’t being triggered. <br>
**Solution:** Ensured `IntersectionObserver` was observing the last video card correctly and that `hasNextPage` was set properly in response.

#### 2. Cursor Value Was Incorrect
**Problem:** API returned null `nextCursor` even when more videos existed  <br>
**Solution:** Applied the "n+1" pattern by fetching one extra video and using its ID as the cursor for the next page

#### 3. Video List Re-rendered on Every Fetch
**Problem:** All videos re-rendered after fetching next page <br> 
**Solution:** Used `flatMap()` across `data.pages` and memoized the list
