# 🧩 Dev Stack Builder

**Dev Stack Builder** is a responsive web application built with React and TypeScript. It provides a collection of commonly used development technologies and allows users to create a personalized tech stack by selecting the technologies they want.

The application organizes technologies into different categories such as frontend, backend, databases, programming languages, styling tools, and DevOps.

## 🛠️ Tech Stack

- **React.js** — UI development
- **TypeScript** — Type-safe JavaScript development
- **Vite** — Development server and build tool
- **Tailwind CSS** — Styling and responsive design
- **React-Toastify** — User notifications
- **JSON** — Local technology information

## 🌟 Main Features

### 1. Build Your Own Stack

Users can add technologies from the available technology cards to their personal stack. Selected items are displayed in a separate sidebar and can also be removed when needed.

### 2. Prevent Duplicate Selection

Once a technology has been selected, its button changes to an **"✓ Added to Stack"** state. This prevents the same technology from being added multiple times and provides feedback through toast notifications.

### 3. Responsive Design

The interface is designed to work across different screen sizes. The technology cards use a responsive grid layout, while the navigation also adapts for smaller devices with a mobile menu.

---

# 📚 React Questions & Answers

## 1. What is JSX, and why is it used in React?

**Answer:**

JSX is a JavaScript syntax extension that allows us to write markup that looks similar to HTML directly inside JavaScript or TypeScript code.

It makes React components easier to understand because the structure of the UI can be written close to the logic that controls it.

---

## 2. What is the difference between props and state?

**Answer:**

**Props** are values passed from a parent component to a child component. They are mainly used to share data between components.

**State** is data managed inside a component that can change during the application's execution. When state changes, React updates the related UI.

For example, in this project, technology information can be passed through props, while the selected stack is maintained using state.

---

## 3. What does the `useState` hook do, and where did you use it in this project?

**Answer:**

`useState` is a React Hook that allows a functional component to store and update information that may change over time.

In this project, I used `useState` to keep track of the technologies selected by the user for the **Your Stack** section.

---

## 4. What does the `useEffect` hook do, and why did you need it to load the JSON data?

**Answer:**

`useEffect` is a React Hook used for handling side effects such as loading data, making API requests, or interacting with external resources.

I used it when the component loads so that the technology information from the local JSON file can be loaded and made available to the application.

---

## 5. Why does every item in a `.map()` list need a unique `key` prop?

**Answer:**

React needs a unique `key` for each item in a rendered list so that it can recognize which items have changed, been added, or been removed.

Using a stable identifier such as `technology.id` helps React update the list more efficiently.

### Example:

```jsx
{
  technologies.map((technology) => (
    <TechnologyCard key={technology.id} technology={technology} />
  ));
}
```

---

## 6. What is conditional rendering? Show one place you used it.

**Answer:**

Conditional rendering means displaying different parts of the interface depending on whether a particular condition is true or false.

In this project, I used conditional rendering in the **Your Stack** section. When the user has not selected any technology, an empty-state message is displayed. Otherwise, the selected technologies are shown.

### Example:

```jsx
{stack.length === 0 ? (
  <p>Your stack is empty</p>
) : (
  // selected technologies
)}
```

---

## 7. How do you pass data from a parent component to a child component, and how does a child send something back to the parent?

**Answer:**

A parent component can provide data to a child component through **props**.

If the child needs to communicate an action back to the parent, the parent can pass a function as a prop. The child can then call that function when a particular event occurs.

### Example:

```jsx
<TechnologyCard technology={technology} onAdd={handleAdd} />
```

Here, `technology` provides the data to the child component, while `onAdd` allows the child to trigger the parent's `handleAdd` function.
