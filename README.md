
# FocusFlow

**FocusFlow** is a full-stack task management application designed to help users track, filter, and manage tasks with attributes like priority, difficulty, status, and deadlines. The system includes user authentication, real-time updates, and responsive UI/UX.

---

## 🛠️ Tech Stack

### Frontend (React)
- React 19 (with React Router v7)
- Bootstrap 5 + React-Bootstrap
- React-Select
- Custom components for filtering, task display, user modals, etc.

### Backend (Flask)
- Flask with SQLAlchemy ORM
- RESTful API endpoints
- SQLite database
- CORS-enabled for frontend/backend communication
- Session-based authentication

### Deployment
- Dockerized frontend and backend
- Managed via `docker-compose`
- Separate containers for `React App` and `Flask API`

---

## 📁 Project Structure

### Frontend (`focus-flow/`)
- `src/API`: API calls (AddTask, GetTasks, Login, etc.)
- `src/Components`: Reusable components (TaskCard, Filter, Header, Modal, etc.)
- `App.js`: Route handling and session checks
- `public/index.html`: Root HTML file
- `.env`: Environment settings
- `Dockerfile`: Docker config for React

### Backend (`focus-flow-api/`)
- `app.py`: Main Flask app and route definitions
- `database.py`: SQLAlchemy models and DB initialization
- `Dockerfile`: Docker config for Flask
- `requirements.txt`: Python dependencies

### Root
- `docker-compose.yaml`: Compose setup for full-stack container orchestration

---

## 🚀 Getting Started

### Prerequisites
- Docker Desktop
- Python 3.10 or higher
- Node.js

### Development Setup

1. Clone the repo:
```bash
git clone https://github.com/your-repo/focus-flow.git
cd focus-flow
```

2. Start the full stack:
```bash
docker-compose up --build
```

3. Access:
- Frontend: [http://localhost:3000](http://localhost:3000)
- Backend API: [http://localhost:5000](http://localhost:5000)

---

## 🧪 Features

- 🔐 **User Authentication** (Register/Login/Logout)
- 📝 **Task CRUD**: Create, Edit, Delete, View
- 🎛️ **Filtering**: By difficulty, priority, and search term
- 📅 **Deadlines**: With validation
- 🌈 **Responsive Design**: Styled with custom CSS and Bootstrap
- 📦 **Task Grouping**: To-Do, In Progress, and Completed lanes
- 💡 **Visuals**: Lightning background, color-coded priorities and difficulties

---

## 🧩 API Overview

- `POST /register`: Register new user
- `POST /login`: Login user
- `GET /logout`: Logout current user
- `GET /currentuser`: Fetch session user
- `GET /tasks`: Get filtered task list
- `POST /tasks`: Add task
- `PUT /tasks/<id>`: Edit task
- `DELETE /tasks/<id>`: Remove task
- `GET /priorities`, `GET /difficulties`, `GET /statuses`: Load metadata

---

## 📬 Contact

For issues or contributions, feel free to open an issue or PR.

---

## 📄 License

This project is provided for educational and demo purposes.
