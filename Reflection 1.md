## PRACTICAL 1 : TikTok
### Key Concepts Applied

1. **Next.js App Router & File System Routing**     Used for page creation with clean structure and scalability.

2. **Tailwind CSS**  
Simplified styling with utility-first approach. Clean and fast UI development.

3. **React Components & Layouts**  
Reused layout via `MainLayout.jsx` and organized UI elements like `VideoCard`.

4. **React Hook Form**  
Efficient form state management, validation, and submission handling.

5. **Form Validation Techniques**  
- Required fields
- Pattern matching (email)
- Length constraints
- Custom password confirmation validation


### What I Learned

- How to set up a Next.js project with the new App Router
- Creating a reusable layout system for a multi-page app
- Building responsive UI with Tailwind
- Structuring components and pages efficiently
- Implementing and validating forms using `react-hook-form`


### Challenges Faced

1. **Tailwind Setup Issues**
   - Problem: Initial build failed due to missing PostCSS config
   - Solution: Followed [Tailwind + Next.js guide](https://tailwindcss.com/docs/installation/framework-guides/nextjs)

2. **Layout Not Updating**
   - Problem: Layout changes didn’t reflect in the app
   - Solution: Realized I needed to update `layout.js` in `src/app`

3. **Form Validation Confusion**
   - Problem: Custom validation for password confirmation didn’t work
   - Solution: Used `validate` function inside `react-hook-form` with dependency on `watch()` values

4. **Navigation Links**
   - Problem: Links to new pages weren’t working
   - Solution: Ensured correct usage of `<Link>` from `next/link` with proper path casing
