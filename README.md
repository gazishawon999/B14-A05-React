# 🧩 Dev Stack Builder

**Dev Stack Builder** is a responsive web application built with **React and TypeScript**. It provides a collection of commonly used development technologies and allows users to create a personalized tech stack by selecting the technologies they want.

The application organizes technologies into different categories such as frontend, backend, databases, programming languages, styling tools, and DevOps.

## 🌐 Live Demo

🚀 **[Visit Dev Stack Builder](https://b14-a05-react-git-main-gazishawon999.vercel.app/)**

---

## 🛠️ Technologies Used

- **React.js** — Building the user interface
- **TypeScript** — Type-safe JavaScript development
- **Vite** — Development and build tool
- **Tailwind CSS** — Styling and responsive layouts
- **React-Toastify** — Toast notifications
- **JSON** — Local technology dataset

---

## ✨ Features

### 1. Build Your Own Stack

Users can browse different technologies and add the ones they prefer to their personal stack. Selected technologies appear in the **Your Stack** section and can be removed whenever needed.

### 2. Duplicate Selection Protection

A technology that has already been selected cannot be added again. Its button changes to **"✓ Added to Stack"**, and the application provides feedback through toast notifications.

### 3. Technology Categories

The application contains technologies from several areas, including:

- Frontend
- Backend
- Database
- Programming Languages
- Styling
- DevOps

### 4. Responsive Interface

The application is designed to provide a smooth experience on different screen sizes. The technology cards use a responsive grid layout, and the navigation adapts to smaller devices.

### 5. Interactive User Feedback

Toast notifications are used to inform users when technologies are added, removed, or when they attempt an invalid action.

---

# 📚 React Questions & Answers

## 1. What is JSX, and why is it used in React?

**Answer:**

JSX is a syntax extension for JavaScript that allows us to write HTML-like markup directly inside JavaScript or TypeScript code.

It makes React components easier to read and helps developers describe the structure of the user interface in a clear way.

---

## 2. What is the difference between props and state?

**Answer:**

**Props** are used to pass data from a parent component to a child component. They allow components to communicate with each other.

**State** is data that is managed inside a component and can change during the application's execution. When the state changes, React updates the related part of the UI.

In this project, technology information is passed through props, while the selected technologies are managed using state.

---

## 3. What does the `useState` hook do, and where did you use it in this project?

**Answer:**

`useState` is a React Hook that allows a functional component to store and update data that can change over time.

In this project, I used `useState` to manage the technologies selected by the user in the **Your Stack** section.

---

## 4. What does the `useEffect` hook do, and why did you need it to load the JSON data?

**Answer:**

`useEffect` is a React Hook used for handling side effects in a component. These can include loading data, making API requests, or interacting with external resources.

In this project, it is used when the component loads to retrieve the technology information from the local JSON file.

---

## 5. Why does every item in a `.map()` list need a unique `key` prop?

**Answer:**

React uses the `key` prop to uniquely identify items in a list. It helps React determine which items have changed, been added, or removed.

Using a unique and stable value such as `technology.id` allows React to update the list efficiently.

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

Conditional rendering means displaying different UI elements depending on whether a particular condition is true or false.

In this project, conditional rendering is used in the **Your Stack** section. If the user has not selected any technology, an empty-state message is displayed. Otherwise, the selected technologies are shown.

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

A parent component passes data to a child component through **props**.

To allow a child component to communicate an action back to its parent, the parent can pass a function as a prop. The child can then call that function when a specific event occurs.

### Example:

```jsx
<TechnologyCard technology={technology} onAdd={handleAdd} />
```

Here, `technology` passes information to the child component, while `onAdd` allows the child component to trigger the `handleAdd` function defined in the parent.

---

## 📁 Project Structure

A simplified structure of the project looks like this:

```text
Dev-Stack-Builder/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   ├── data/
│   ├── App.tsx
│   ├── main.tsx
│   └── index.css
├── package.json
├── tsconfig.json
├── vite.config.ts
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Move into the project directory

```bash
cd Dev-Stack-Builder
```

### 3. Install dependencies

```bash
npm install
```

### 4. Start the development server

```bash
npm run dev
```

The application will then be available through the local development URL provided by Vite.

---

## 📦 Build for Production

To create a production build:

```bash
npm run build
```

To preview the production build locally:

```bash
npm run preview
```

---

## 🌍 Deployment

The project is deployed using **Vercel**.

🔗 **Live Website:**
https://b14-a05-react-one.vercel.app/

or

https://b14-a05-react-git-main-gazishawon999.vercel.app/

---

## 👨‍💻 Author

**Shawon Gazi**

- GitHub: https://github.com/gazishawon999
- LinkedIn: https://www.linkedin.com/in/gazishawon999/

---

## 📄 License

This project was created for learning and educational purposes.
