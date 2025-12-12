# ⚽ FIFA26 – Full Stack Web Application

FIFA26 is a full-stack web application developed as part of the **Full Stack Development** module.  
The application allows users to authenticate securely and browse football player data through a modern, responsive Angular frontend supported by a Python Flask backend.

---

## 📌 Project Overview

The FIFA26 application demonstrates core full-stack development concepts, including:

- Frontend development using Angular
- Backend development using Python Flask
- RESTful API communication
- Authentication and authorization
- Responsive UI design
- Testing and performance evaluation

The system is designed to be modular, maintainable, and easy to extend.

---

## ✨ Features

- User registration and login
- Token-based authentication
- Route protection using Angular guards
- Dynamic navigation bar based on login state
- Player listing with images
- Search functionality
- Pagination for efficient browsing
- Responsive design for desktop and mobile devices
- Performance testing using Lighthouse

---

## 🛠️ Tech Stack

### Frontend
- Angular
- TypeScript
- HTML5
- SCSS
- Bootstrap
- RxJS

### Backend
- Python
- Flask
- RESTful API
- HTTP Basic Authentication
- Token-based session handling

### Tools
- Git & GitHub
- Chrome DevTools
- Lighthouse

---

## 🏗️ System Architecture

The application follows a **client–server architecture**:

- **Frontend (Angular)**  
  Handles routing, UI rendering, user interaction, and state management.

- **Backend (Flask)**  
  Manages authentication endpoints and session handling.

- **Data Source**  
  Player data is loaded from a local JSON file located in the frontend assets directory.  
  This approach simplifies backend complexity while still supporting all frontend features such as search and pagination.

---

## 📁 Project Structure

fifa26-project/
│
├── backend/
│ ├── app.py
│ ├── auth.py
│ └── requirements.txt
│
├── fifa26-frontend/
│ ├── angular.json
│ ├── package.json
│ ├── tsconfig.json
│ ├── download_faces.py
│ ├── transform.py
│ │
│ └── src/
│ ├── index.html
│ ├── main.ts
│ ├── styles.scss
│ ├── environment/
│ │ └── environment.ts
│ │
│ └── app/
│ ├── components/
│ ├── services/
│ ├── models/
│ ├── guards/
│ └── interceptors/

yaml
Copy code

---

## 🌐 API Endpoints

| Endpoint | Method | Description |
|--------|--------|-------------|
| `/register` | POST | Registers a new user |
| `/login` | GET | Authenticates user and returns token |
| `/logout` | POST | Logs out authenticated user |

### Static Data
- `assets/players_simplified.json`  
  Used to load player data for listing, searching, and pagination.

---

## 🔐 Authentication Flow

1. User registers via `/register`
2. User logs in via `/login`
3. Backend validates credentials and returns a token
4. Token is stored in the browser
5. Angular HTTP interceptor attaches the token to requests
6. Route guard restricts protected pages
7. Logout clears the token and resets application state

---

## 🧪 Testing

The application has been tested using:

- Authentication testing (register, login, logout)
- Guard redirect testing for protected routes
- Player list rendering tests
- Search and pagination testing
- Navbar state testing
- Responsive layout testing
- Performance testing using Lighthouse
- Browser DevTools performance metrics

Detailed testing evidence and screenshots are provided in the **Application Testing Report**.

---

## ⚙️ Installation & Setup

### Frontend Setup
```bash
cd fifa26-frontend
npm install
Backend Setup
bash
Copy code
cd backend
pip install -r requirements.txt
python app.py
▶️ Running the Application
Start Backend
bash
Copy code
python app.py
Start Frontend
bash
Copy code
ng serve
Open the application in your browser at:

arduino
Copy code
http://localhost:4200
🚀 Future Improvements
Replace local JSON with a full backend player API

Add user roles (admin/user)

Improve error handling and validation

Increase automated test coverage

Deploy application using Docker or cloud services

👤 Author
Shree Nepal
Student ID: 10191960
Module: Full Stack Development

