# 🔢 React Counter App

A simple and clean React application demonstrating **state management** using the `useState` hook. The app contains a single reusable `Counter` component with increment and decrement functionality. This repository is ideal for beginners learning React fundamentals and Vite setup.

---

## 📸 Output Screenshot

> Save the screenshot image in your repository (recommended path: `assets/screenshot.jpg`) and the image will render below.

```markdown
![Counter App Screenshot](./assets/screenshot.jpg)
```

> **Note:** If you prefer a different filename or path (for example `screenshot.png` in the repo root), adjust the path above accordingly.

---

## 🚀 Project Overview

* **Framework:** React (Functional Components)
* **Build tool:** Vite
* **Concepts demonstrated:** `useState`, component composition, event handling, controlled UI
* **No backend:** All state is client-side and resets on refresh

---

## 📁 Project Structure

```
my-react-counter-app/        # repository root
├── assets/                  # static assets (add your screenshot here)
│   └── screenshot.jpg       # <-- add your output screenshot here
├── node_modules/            # dependencies (auto-generated)
├── public/                  # (optional) public static files
├── src/
│   ├── App.jsx              # main app that mounts the Counter component
│   ├── App.css              # global styles
│   └── component/
│       └── Counter.jsx      # Counter component (useState hook example)
├── .gitignore
├── index.html
├── package.json
├── package-lock.json
└── README.md                # this file
```

---

## 📘 Files (short explanation)

* `src/App.jsx` – The root component that renders `<Counter />`.
* `src/component/Counter.jsx` – The counter component: has local state (`count`) and `increment` / `decrement` handlers.
* `src/App.css` – Optional stylesheet to style the app and center the UI.
* `assets/screenshot.jpg` – The output screenshot to show in README (add this file to repo).
* `package.json` – Project metadata and scripts.

---

## 📄 Full Example Code

### `src/App.jsx`

```jsx
import { useState } from 'react'
import './App.css'
import Counter from './component/Counter'

function App() {
  return (
    <>
      <Counter />
    </>
  )
}

export default App
```

### `src/component/Counter.jsx`

```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  const increment = () => setCount(c => c + 1);
  const decrement = () => setCount(c => c - 1);

  return (
    <div className="container">
      <h1>Counter</h1>
      <h2>{count}</h2>
      <div className="buttons">
        <button onClick={increment}>increment</button>
        <button onClick={decrement}>decrement</button>
      </div>
    </div>
  );
}

export default Counter;
```

### `src/App.css` (suggested)

```css
body, html, #root {
  height: 100%;
  margin: 0;
  font-family: Inter, system-ui, -apple-system, Roboto, 'Segoe UI', Arial;
}

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

h1 { font-size: 48px; color: #17394a; }

h2 { font-size: 28px; margin: 12px 0; }

.buttons button {
  margin: 0 8px;
  padding: 10px 18px;
  border-radius: 8px;
  border: 1px solid #111;
  background: white;
  cursor: pointer;
}
```

---

## ▶️ How to Run (Vite)

1. Install dependencies

```bash
npm install
```

2. Start the dev server

```bash
npm run dev
```

3. Open the app

```
http://localhost:5173
```

If your `package.json` uses a different script, use the appropriate command (for example `npm start` for CRA).

---

## ✅ Add screenshot to README (quick steps)

1. Create an `assets/` folder in repo root.
2. Copy your screenshot file (from your PC) into `assets/` and rename it `screenshot.jpg`.
3. Commit and push to GitHub:

```bash
git add assets/screenshot.jpg README.md
git commit -m "Add README and screenshot"
git push
```

4. GitHub will render the image in the README automatically.

---

## 🔖 Badges (optional)

You can add these at the top of README for polish:

```
![Vite](https://img.shields.io/badge/Vite-~4.0-646cff)
![React](https://img.shields.io/badge/React-17.x-61dafb)
```

---

## 🤝 Contributing

Contributions and improvements are welcome. Feel free to open issues or pull requests.

---

## 📜 License

MIT © Your Name

---

If you'd like, I can:

* create the `assets/` folder and add the screenshot file to the repo for you (if you provide a link), or
* generate a downloadable `README.md` file here so you can paste it into your repo.

Which would you like next?
