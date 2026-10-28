# Real-Time Text Editor

A real-time collaborative text editor built using **React, Monaco Editor, Yjs, Socket.IO, and Express.js**. It allows multiple users to collaborate on the same document with real-time text synchronization.

## Features

- **Real-Time Collaborative Editing:** Synchronizes text changes between connected users.
- **Monaco Editor Integration:** Provides a modern text-editing experience.
- **Username-Based Joining:** Allows users to join using a username.
- **Active Users List:** Displays connected participants.
- **Real-Time Communication:** Uses Socket.IO for client-server communication.
- **Collaborative Synchronization:** Uses Yjs to manage shared document updates.
- **Backend Server:** Uses Node.js and Express.js.
- **Health Check Endpoint:** Provides a `/health` endpoint to check server status.
- **Docker Support:** Uses a multi-stage Docker build to build the frontend and package it with the backend.

## Technologies Used

- **Frontend:** React, Vite, Monaco Editor
- **Backend:** Node.js, Express.js
- **Real-Time Communication:** Socket.IO
- **Collaboration Framework:** Yjs, y-socket.io
- **Containerization:** Docker
- **Version Control:** Git and GitHub

## Project Structure

```text
Real-Time-Text-Editor/
├── backend/
│   ├── package.json
│   └── server.js
├── frontend/
│   ├── package.json
│   └── src/
├── .dockerignore
├── dockerfile
└── README.md
```

## How It Works

1. Users open the text editor in their browser.
2. Each user joins using a username.
3. The frontend connects to the backend.
4. Socket.IO enables real-time communication.
5. Yjs synchronizes collaborative document changes.
6. Connected users can edit the shared document and see updates in real time.

## Prerequisites

To run the project locally, install:

- [Node.js](https://nodejs.org/)
- npm

To run the project with Docker, install [Docker Desktop](https://www.docker.com/products/docker-desktop/).

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Touhidur25/Real-Time-Text-Editor.git
```

### 2. Navigate to the Project

```bash
cd Real-Time-Text-Editor
```

### 3. Install Backend Dependencies

```bash
cd backend
npm install
```

### 4. Start the Backend

```bash
npm start
```

### 5. Run the Frontend

Open a separate terminal:

```bash
cd frontend
npm install
npm run dev
```

Open the local URL displayed by Vite in your terminal.

## Running with Docker

This project uses a multi-stage Docker build. The first stage builds the frontend, and the second stage installs the backend dependencies and copies the frontend build into the backend's `public` directory.

### 1. Build the Docker Image

Run from the project root directory:

```bash
docker build -t real-time-text-editor -f dockerfile .
```

### 2. Run the Container

```bash
docker run -d --name real-time-text-editor -p 3000:3000 real-time-text-editor
```

Open `http://localhost:3000` in your browser, assuming the backend listens on port `3000`.

### 3. Check Container Logs

```bash
docker logs real-time-text-editor
```

### 4. Stop the Container

```bash
docker stop real-time-text-editor
```

### 5. Remove the Container

```bash
docker rm real-time-text-editor
```

**Note:** Adjust the port mapping according to the port configured in `backend/server.js`.

## Health Check

The backend provides a health check endpoint:

```http
GET /health
```

Use this endpoint to check whether the backend server is responding.
