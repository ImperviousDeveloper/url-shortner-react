# 🌐 URL Shortener Application

## 🚀 Introduction

The **URL Shortener Application** is a sleek and modern web solution built with **React** on the frontend and **Spring Boot** on the backend. This application allows users to shorten long URLs into more manageable links and track the number of visits for each shortened URL.

## ✨ Features

- 🔗 Generate short URLs instantly
- 📊 Track the number of clicks on shortened URLs
- 🧑‍💻 REST API for URL shortening and analytics
- 🌍 Customizable short links (optional feature)
- 🏎️ Lightning-fast performance with React & Spring Boot

## 🛠️ Tech Stack

### Frontend

- React
- React Router
- Axios
- TailwindCSS 

### Backend

- Spring Boot
- Spring Data JPA
- Hibernate
- PostgreSQL (or H2 for local development)
- Lombok

## 📦 Installation & Setup

### Prerequisites

- Java 17+
- Node.js & npm
- PostgreSQL (or Docker if preferred)

### Backend Setup

```bash
cd backend
./mvnw clean install
./mvnw spring-boot:run
```

### Frontend Setup

```bash
cd frontend
npm install
npm start
```

## 🧑‍💻 API Endpoints

| Method | Endpoint              | Description                     |
|--------|------------------------|----------------------------------|
| POST   | /api/v1/shorten        | Shorten a URL                   |
| GET    | /api/v1/{shortCode}    | Redirect to the original URL    |
| GET    | /api/v1/stats/{shortCode} | Get visit count for a short URL |

## ⚙️ Environment Variables

Create a `.env` file in both `backend` and `frontend` directories:

### Backend `.env`:

```env
DATABASE_URL=jdbc:postgresql://localhost:5432/url_shortener
DATABASE_USERNAME=your_db_user
DATABASE_PASSWORD=your_db_password
```

### Frontend `.env`:

```env
REACT_APP_API_BASE_URL=http://localhost:8080/api/v1
```

## 🖼️ Screenshots

![Homepage](https://via.placeholder.com/600x300?text=Homepage+Screenshot)
![Shortened URL](https://via.placeholder.com/600x300?text=Shortened+URL+Screenshot)

## 🧪 Testing

- Frontend Unit Tests with Jest & React Testing Library
- Backend Tests with JUnit & MockMVC

## 🚀 Future Enhancements

- ✅ User Authentication for personalized URL tracking
- ✅ Custom domain support for short URLs
- ✅ QR code generation for short links
- ✅ Expiry dates for short URLs

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repository and open a pull request.

## 📫 Contact

- **Email:** [mr.sharmajeerajan@gmail.com](mailto:mr.sharmajeerajan@gmail.com)

- **LinkedIn:** [LinkedIn Profile](https://www.linkedin.com/in/rajan-kumar-sharma-709a17229/)

---

> "Great software is built by passionate developers."

