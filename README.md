# Frontend-interview-Notes
Some vip concept
# Frontend Concepts Explained Simply

## 1. Hydration
When a server sends HTML to the browser (Server-Side Rendering), the page looks ready but isn't interactive yet. **Hydration** is the process where React (or similar frameworks) attaches event listeners and makes the page fully interactive, without re-rendering the entire DOM.

---

## 2. Partial Hydration
Instead of hydrating the whole page at once, only specific interactive parts are hydrated. The rest of the page remains static. This improves performance by reducing JavaScript work on initial load.

---

## 3. Islands Architecture
A web page is treated as a collection of independent "islands" of interactivity. Each island can be loaded and hydrated separately. Static content surrounds them. This is used in frameworks like Astro or Fresh.

---

## 4. Streaming SSR
Server sends HTML in chunks as soon as it's ready, instead of waiting for the whole page. The browser can start rendering parts of the page earlier, improving perceived performance.

---

## 5. Concurrent Rendering
A React feature that lets rendering be interruptible. The app can prepare multiple UI versions at the same time without blocking the main thread, making it more responsive.

---

## 6. Time Slicing
Breaks rendering work into small chunks spread over multiple frames. This prevents the UI from freezing during heavy updates, keeping animations and interactions smooth.

---

## 7. Reconciliation Algorithm
The process React uses to compare the previous and new virtual DOM trees and figure out the most efficient way to update the real DOM.

---

## 8. Fiber Architecture
React's new core algorithm (introduced in React 16). It enables features like concurrent rendering, time slicing, and better handling of updates by breaking work into units (fibers) and prioritizing them.

---

## 9. Virtual DOM Diffing Complexity
When comparing two virtual DOM trees, React uses a heuristic (assumptions) to make it faster — usually **O(n)** complexity, where n is the number of elements, instead of the theoretical O(n³).

---

## 10. Structural Sharing
Used in immutable data structures (like in Redux or Immer). When updating an object, unchanged parts are reused (shared) instead of copied, saving memory and improving performance.

---

