# 🔗 URL Shortener App

An efficient and modern URL Shortener application built with **React (Frontend)** and **Spring Boot (Backend)**. It helps you shorten long URLs into short, manageable links.

## 🚀 Live Demo

🔗 [View the Live App](https://<your-github-username>.github.io/<repository-name>)

## 📦 Features

- 🧑‍💻 **Custom Short URLs**: Generate short links from long URLs.
- 📊 **Analytics Tracking**: Track the number of visits on each short URL.
- 🎨 **Modern UI**: Built with React, styled with Tailwind CSS & Framer Motion animations.
- ⚡ **Fast and Reliable**: Powered by Spring Boot backend.
- 🌐 **Deployed with GitHub Pages**.

## 🛠️ Tech Stack

**Frontend:**
- React
- Vite
- Tailwind CSS
- Framer Motion (Animations)

**Backend:**
- Spring Boot
- Java
- Hibernate / JPA

## 📂 Project Structure
```
url-shortener-app/
│
├── backend/         # Spring Boot application
│   └── src/
│
├── frontend/        # React Vite application
│   └── src/
│
└── README.md
```

## 🏃‍♂️ Getting Started

### 🖥️ Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

### ⚙️ Backend Setup

```bash
cd backend
./mvnw spring-boot:run
```

## 🚀 Deployment (Frontend to GitHub Pages)

### 1. Install gh-pages
```bash
npm install gh-pages --save-dev
```

### 2. Update `package.json`
```json
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d dist"
}
```

### 3. Configure `vite.config.js`
```javascript
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()],
  base: '/<repository-name>/',
});
```

### 4. Deploy
```bash
npm run deploy
```

## 📷 Screenshots
| Home Page | Shortened URL |
|-----------|---------------|
| ![Home](https://via.placeholder.com/300) | ![Shortened URL](https://via.placeholder.com/300) |

## 📬 Contact
- **GitHub**: [@YourUsername](https://github.com/YourUsername)
- **LinkedIn**: [Your Profile](https://linkedin.com/in/yourprofile)

---

⭐ **Star this repo if you found it helpful!**

