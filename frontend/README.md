# Frontend Setup – Fullstack Chat App

This README provides a step-by-step guide to setting up the frontend part of the Fullstack Chat App.

---

## 📦 Tech Stack

- React.js
- Zustand (state management)
- Tailwind CSS + PostCSS (styling)
- Axios (HTTP requests)
- Socket.IO Client (real-time messaging)

---

## 🔧 Setup Instructions
       
### 1. Clone the Repository

```bash
git clone https://github.com/your-username/fullstack-chat-app.git
cd fullstack-chat-app/frontend
```
### 2. Install Required Dependencies

Install core libraries:

Install Tailwind CSS and PostCSS:
```bash
npm install -D tailwindcss postcss autoprefixer npx tailwindcss init -p
```
---

## 🎨 Tailwind CSS Configuration

### 1. Update `tailwind.config.js`

```
module.exports = { content: [ "./src/**/*.{js,jsx,ts,tsx}", ], theme: { extend: {}, }, plugins: [], }
```

### 2. Add Tailwind Directives to CSS

In `src/index.css` or `src/App.css`, add the following:
```
@tailwind base; @tailwind components; @tailwind utilities;
```

```
Ensure the CSS file is imported in `src/index.js`:
```

---

## 🌐 Axios Setup

Create a file at `src/api/axios.js` and add:
```bash
import axios from 'axios';

const api = axios.create({ baseURL: 'http://localhost:5001/api', // Change this to your backend URL withCredentials: true, });

export default api;
```
---

## 🔌 Socket.IO Client Setup

You can initialize a socket connection like this:

import { io } from 'socket.io-client';

const socket = io('http://localhost:5001'); // Replace with your backend address export default socket;


---

## 🚀 Start the App
```
Visit: http://localhost:5137
```

# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh
