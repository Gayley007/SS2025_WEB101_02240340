## Practical 6 – State Management with Zustand: Todo List App

### Project Overview
In this practical, we created a **Todo List application** using **React** and **Zustand** for state management. Zustand provides a simpler and more lightweight alternative to Redux and React Context by enabling direct state and action access via custom hooks.

### Project Setup

#### Step 1: Initialize Project
```bash
npx create-vite@latest todo-zustand
cd todo-zustand
npm install zustand
```

#### Step 2: Create Zustand Store (src/store/todoStore.js)
Uses create from Zustand <br>
State: todos array <br>
Actions:
  - addTodo
  - toggleTodo
  - removeTodo
  - clearCompleted

#### Step 3: Build Components
**TodoInput.jsx** — adds new todos <br>
**TodoItem.jsx** — displays and toggles a single todo <br>
**TodoList.jsx** — renders all todos <br>

#### Step 4: App Integration
Import and render all components in App.js

### Persistence with localStorage
Used persist middleware from Zustand to:
- Automatically save todos to localStorage
- Rehydrate state on page reload
```js 
import { create } from 'zustand';
import { persist } from 'zustand/middleware';

const useTodoStore = create(persist(
  (set) => ({
    todos: [],
    addTodo: (text) => { ... },
    toggleTodo: (id) => { ... },
    removeTodo: (id) => { ... },
    clearCompleted: () => { ... },
  }),
  { name: 'todo-storage' }
));
```

### Key Concepts
Zustand simplifies global state by:
- Avoiding prop drilling
- Reducing boilerplate compared to Redux
- Reactively updating only subscribed components

### Dependencies
- React
- Zustand