# 🌟 React Interview Questions and Answers

### 1. What is React?

React is a **JavaScript library** developed by Facebook for building **user interfaces**, especially for single-page applications where a dynamic and interactive user experience is essential. It allows developers to create reusable UI components and efficiently update and render the right components when data changes.

### 2. What are components in React?

Components are the **building blocks** of a React application. They represent parts of the UI and allow developers to split the UI into **independent, reusable pieces**. Each component can manage its own state and logic. Components can be either **functional** or **class-based**.

### 3. What is JSX?

JSX stands for **JavaScript XML**. It is a **syntax extension** for JavaScript that looks similar to HTML. JSX makes it easier to write and add HTML-like code directly in JavaScript files, allowing React components to be more expressive and intuitive.

### 4. What is the difference between functional and class components?

- **Functional components** are simple JavaScript functions that return JSX.
- **Class components** are ES6 classes that extend `React.Component` and have additional features like lifecycle methods and local state (before hooks were introduced).

Today, **functional components with hooks** are preferred due to simplicity and better performance.

### 5. What are props in React?

Props (short for **properties**) are read-only inputs passed from a parent component to a child component. They allow data to flow from parent to child and help make components **dynamic and reusable**. Props cannot be modified by the receiving component.

### 6. What is state in React?

State is a built-in object that allows components to **store data** about themselves. Unlike props, state is **mutable** and is used to manage data that changes over time, such as user input, toggles, or fetched data.

### 7. What is the difference between state and props?

- **Props** are passed to the component and are **read-only**.
- **State** is managed within the component and can be **changed** using specific methods (like hooks).

Props are used for **external configuration**, while state is used for **internal data handling**.

### 8. What is a controlled component?

A controlled component is a form input element (like `<input>`, `<textarea>`, etc.) whose value is controlled by the component’s state. The React component that renders the form also controls what happens in that form on user input.

### 9. What is the Virtual DOM?

The Virtual DOM is a **lightweight in-memory representation** of the real DOM elements. When a component’s state or props change, React updates the Virtual DOM first, compares it with the previous version, and then updates only the necessary parts of the real DOM. This makes updates **fast and efficient**.

### 10. What is the purpose of keys in React lists?

Keys help React **identify which items have changed**, are added, or are removed. They are essential when rendering lists to ensure React can efficiently update and re-render elements. A key should be **unique** among siblings.

### 11. What is lifting state up in React?

Lifting state up means moving the shared state to the **closest common ancestor** of the components that need access to that state. This allows for better synchronization and communication between child components through props.

### 12. What are hooks in React?

Hooks are special functions that let you **use state and other React features** in functional components. They allow functional components to have side effects, manage local state, context, and more—making class components largely unnecessary for most use cases.

### 13. What is useState hook?

The `useState` hook allows you to **add local state** to a functional component. It returns a state variable and a function to update it, letting components respond to user input or other dynamic data.

### 14. What is useEffect hook?

The `useEffect` hook lets you perform **side effects** (like data fetching, subscriptions, or manual DOM changes) in function components. It runs after render and can optionally clean up before the next effect runs or when the component unmounts.

### 15. How does React handle forms?

React handles forms using **controlled components**, where form inputs derive their values from state and update that state via event handlers. This keeps the form input data in sync with the React component state.

### 16. What is prop drilling?

Prop drilling is the process of **passing props through multiple nested components** even if only the deeply nested child needs them. This can make components harder to maintain.

### 17. What is context API in React?

The Context API allows data to be shared across the component tree **without passing props manually at every level**. It’s useful for global data like themes, user information, or language preferences.

### 18. How can you optimize performance in a React app?

React app performance can be optimized using techniques like:

- Memoization (`React.memo`, `useMemo`, `useCallback`)
- Lazy loading components
- Code splitting
- Avoiding unnecessary re-renders
- Efficient list rendering with keys
- Using the Production build

### 19. What is React Router?

React Router is a **routing library** for React that allows navigation between different components/pages. It keeps the UI in sync with the URL and enables features like nested routes, dynamic routing, and route protection.

### 20. What are React fragments?

React Fragments allow you to **group multiple elements** without adding extra nodes to the DOM. This is useful when returning multiple elements from a component without wrapping them in an unnecessary `<div>`.

---

### **21. What is the difference between `useMemo` and `useCallback`?**

- `useMemo` is used to **memoize a computed value**, preventing unnecessary recalculations unless its dependencies change.
- `useCallback` is used to **memoize a function**, so it’s not recreated unless its dependencies change.

Both help with **performance optimization** by avoiding unnecessary work on re-renders.

---

### **22. What are render props in React?**

Render props is a pattern where a **function is passed as a prop** to a component, allowing the component to decide what to render. It enables **code sharing** and **reusability**, especially in components that handle common logic but render differently.

---

### **23. What is the purpose of error boundaries in React?**

Error boundaries are components that **catch JavaScript errors** anywhere in their child component tree, log those errors, and display a fallback UI. They do **not catch errors in event handlers**, but they’re critical for ensuring that errors don’t crash the entire UI.

---

### **24. What is the difference between Server-Side Rendering (SSR) and Client-Side Rendering (CSR)?**

- **SSR**: React components are rendered on the **server**, and the browser receives a fully rendered HTML page. This improves SEO and speeds up the first page load.
- **CSR**: The browser downloads a bare HTML page and then uses JavaScript to render the React components. This provides a dynamic experience but may be slower to show content initially.

---

### **25. What is hydration in React?**

Hydration is the process where **React attaches event handlers** to the pre-rendered HTML content (usually generated by SSR). It turns the static HTML into a **fully interactive React application** without re-rendering the entire page.

---

### **26. What is `React.lazy` and how is it used?**

`React.lazy` allows you to **dynamically import** components only when they’re needed, which reduces the initial load time. It’s part of **code splitting** and works well with `Suspense` to show a fallback while loading.

---

### **27. What are custom hooks in React?**

Custom hooks are **reusable functions** that use built-in hooks like `useState`, `useEffect`, etc. They start with `use` and let you **encapsulate logic** that can be shared across multiple components, improving maintainability.

---

### **28. What are Portals in React?**

Portals let you render a component's children **into a different part of the DOM** than its parent component. This is useful for modals, tooltips, or dropdowns that need to break out of parent layout constraints.

---

### **29. What is tree shaking and how does React benefit from it?**

Tree shaking is a **build optimization technique** that removes unused code from the final JavaScript bundle. React and modern bundlers like Webpack support this, helping reduce app size and improve performance.

---

### **30. What are forward refs in React?**

`forwardRef` is a technique to **pass a ref from a parent to a child component**, allowing the parent to directly reference a DOM element or component instance inside the child. It’s especially useful for managing focus or animations.
