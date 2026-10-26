# Real-Time Text Editor

A real-time collaborative text editor built using Monaco Editor, Yjs, Socket.IO, and Express.js. The application allows multiple users to collaborate on the same text document with real-time synchronization.

## Features

- **Real-Time Collaborative Editing:** Synchronize text changes between connected users in real time.
- **Monaco Editor Integration:** Provides a powerful text editing experience.
- **Username-Based Joining:** Allows users to join the editor using a username.
- **Active Users List:** Displays the usernames of connected participants.
- **Real-Time Communication:** Uses Socket.IO and Yjs to manage collaborative editing and synchronization.
- **Backend Server:** Built with Express.js to handle server-side functionality.
- **Health Check Endpoint:** Provides a `/health` endpoint to check server status.

## Technologies Used

- **Frontend:** Monaco Editor
- **Backend:** Node.js, Express.js
- **Real-Time Communication:** Socket.IO
- **Collaboration Framework:** Yjs


  ## Project Structure

```text
Real-Time-Text-Editor/
├── backend/    # Server-side logic and real-time communication
└── frontend/   # User interface and text editor
```

### Folder Description

- **`backend/`** — Handles server-side functionality and real-time communication between connected users using Express.js and Socket.IO.
- **`frontend/`** — Contains the user interface, Monaco Editor integration, and client-side collaborative editing functionality.
