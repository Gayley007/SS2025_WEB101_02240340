## PRACTICAL 6: State Management with Zustand

### Key Concepts Applied

1. **Zustand Store Creation**
   - Created a centralized store with state (`todos`) and actions (`addTodo`, `toggleTodo`, etc.)
   - Used `create` from Zustand and `persist` middleware for localStorage syncing

2. **Component-Based Architecture**
   - `TodoInput`, `TodoItem`, and `TodoList` followed modular structure
   - Separated UI logic from state logic for better maintainability

3. **Direct State Access via Hooks**
   - Used `useTodoStore((state) => state.todos)` to access data
   - Components only subscribed to what they needed, optimizing re-renders

4. **Persistence with Middleware**
   - Used Zustand's `persist` middleware to store and retrieve todos via `localStorage`


### What I Learned

- Zustand offers a very clean and efficient way to manage state in React
- How to build custom stores that can persist and mutate state
- Avoided prop drilling by letting any component access state directly
- Improved app performance by reducing unnecessary re-renders
- Understood practical middleware usage in state management


### Challenges Faced

#### 1. State Not Persisting After Reload
**Problem:** Todos would disappear on page refresh  
**Solution:** Added `persist` from Zustand and ensured correct `name` and structure were passed.

#### 2. Duplicate Todo Items
**Problem:** Duplicate entries would sometimes appear when rapidly adding todos  
**Solution:** Added basic validation in `addTodo` to ignore empty or duplicate inputs.

#### 3. Components Not Updating on State Change
**Problem:** Some components didn’t reflect updated state  
**Solution:** Ensured each component used the correct selector hook and subscribed to the needed slice of state.
