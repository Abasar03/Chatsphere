# ChatSphere

ChatSphere is a real-time communication platform that enables smooth and interactive messaging between users. It allows users to connect, chat, and engage with others while managing their contacts. Users can send, accept, or decline friend requests, as well as block or remove connections. Additionally, the platform supports story uploads, enabling users to share updates and view stories posted by their friends.

## Table of Contents
- [ChatSphere](#ChatSphere)
- [Project Overview](#project-overview)
- [Key Features](#key-features)
  - [Backend (FastAPI)](#backend-fastapi)
  - [Frontend (ReactJs)](#frontend-reactjs)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Issues Encountered](#issues-encountered)
- [Contributing](#contributing)
- [License](#license)
- [Future Enhancements](#future-enhancements)

## Project Overview

ChatSphere is a comprehensive communication platform featuring user management, real-time chat, friend management, and story sharing functionalities. It uses **FastAPI** and **MySQL** for the backend, and **ReactJs** for the frontend. WebSockets are used for real-time communication.

## Key Features

### Backend (FastAPI)
- **User Authentication**: Secure signup and login with JWT tokens.
- **Real-Time Messaging**: Send and receive messages instantly using WebSockets.
- **Friend Management**: Send, accept, reject, block, and unblock friend requests.
- **Story Feature**: Upload and view stories from friends.
- **Database**: **MySQL** database for storing user and message data.

### Frontend (ReactJs)
- **User Interface**: Developed using **ReactJs** and **Vite** for fast and responsive UI.
- **Real-Time Communication**: Real-time messaging feature with **WebSockets**.
- **Ant Design**: UI components for a clean and user-friendly design.
- **Routing**: Pages and routes managed using **React Router**.

## Technologies Used
- **Backend**: 
  - **FastAPI**
  - **MySQL**
  - **WebSockets**
  - **Pydantic** (for data validation)
  - **JWT Authentication**
- **Frontend**: 
  - **ReactJs**
  - **Vite**
  - **Ant Design**
  - **Axios** for API requests
  - **Socket.io-client** for WebSocket communication

## Installation

### 1. Clone the Repository
```sh
git clone https://github.com/loaferct/ChatSphere.git
cd ChatSphere
```

### 2. Backend Setup
- **Navigate to the backend directory**:
  ```sh
  cd backend
  ```

- **Create a virtual environment**:
  ```sh
  python -m venv venv
  source venv/bin/activate  # On macOS/Linux
  venv/Scripts/activate    # On Windows
  ```

- **Install dependencies**:
  ```sh
  pip install -r requirements.txt
  ```

- **Create a `.env` file** in the root directory and configure your environment variables:
  ```ini
  MYSQL_HOST=your_mysql_host
  MYSQL_USER=your_mysql_user
  MYSQL_PASSWORD=your_mysql_password
  MYSQL_DATABASE=your_database_name
  SECRET_KEY=your_secret_key
  ALGORITHM=HS256
  ACCESS_TOKEN_EXPIRE_MINUTES=30
  ```

- **Run the application**:
  ```sh
  uvicorn main:app --reload
  ```

### 3. Frontend Setup
- **Navigate to the frontend directory**:
  ```sh
  cd frontend
  ```

- **Install dependencies**:
  ```sh
  npm install
  ```

- **Run the frontend application**:
  ```sh
  npm run dev
  ```

### 4. Access the Application
- **Backend API Docs**: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
- **Frontend**: Open [http://localhost:3000](http://localhost:3000) in your browser.

## Usage

After successfully starting both the backend and frontend:
- Register or log in to use ChatSphere's features.
- Use real-time messaging via WebSocket.
- Manage friends and view shared stories.

## Issues Encountered

- **Real-Time Communication**: Implementing WebSockets for instant messaging posed challenges with message synchronization. This was mostly due to compatibilty issues
                               of fastapi websocket.
- **Authentication**: Managing secure login sessions with JWT tokens required special care.
- **Database Integration**: Efficiently syncing FastAPI with MySQL, especially for real-time chat data, was complex.

## Future Enhancements
We plan to add:
- **Push Notifications** for real-time updates.
- **Video and Voice Chat** using **WebRTC**.
- **Full-text search** for better message discoverability.

