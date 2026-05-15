# 💬 Chatty - Real Time Chat Application

A scalable and modern real-time chat application built using React, Node.js, Socket.io, MongoDB, Docker, and Kubernetes.

Developed and maintained by **Abhishek** 🚀

---

# 📝 Introduction

This project aims to provide a real-time chat experience that's both scalable and secure. With a focus on modern technologies, we're building an application that's easy to use and maintain.

# ✨ Features

- 🔥 Real-time messaging using Socket.io
- 🔐 JWT Authentication & Authorization
- 🟢 Online/Offline user status
- 🖼️ Profile image upload
- 🎨 Multiple chat themes
- ⚡ Fast and responsive UI
- 🐳 Dockerized application
- ☸️ Kubernetes deployment support
- 📱 Modern chat interface

---

# 🛠️ Tech Stack

## Frontend

- React.js
- TailwindCSS
- DaisyUI
- Zustand

## Backend

- Node.js
- Express.js
- Socket.io
- MongoDB
- JWT

## DevOps

- Docker
- Docker Compose
- Kubernetes
- Nginx
- Jenkins

---

# 🔧 Prerequisites

Install the following before running the project:

- [Node.js](https://nodejs.org/)
- [Docker](https://www.docker.com/)
- [Git](https://git-scm.com/)
- [Minikube](https://minikube.sigs.k8s.io/docs/)

---

## 📝 Setup .env File:

1. Navigate to the `backend` directory:

```bash
cd backend
```

2. Create a `.env` file and add the following content (modify the values as needed):

```env
MONGODB_URI=mongodb://mongoadmin:secret@mongodb:27017/dbname?authSource=admin
JWT_SECRET=your_jwt_secret_key
PORT=5001
```

> **Note:** Replace `your_jwt_secret_key` with a strong secret key of your choice.

### Clone the Repository

```bash
git clone https://github.com/AbhishekThite387/full-stack_chatApp.git
```

## 🏗️ Build and Run the Application"

Follow these steps to build and run the application:

1. Build & Run the Containers:

```bash
cd full-stack_chatApp
```

```bash
docker-compose up -d --build
```

2. Access the application in your browser:

```
http://localhost
```

---

## 🛠️ Getting Started

Follow these simple steps to get the project up and running on your local Host using docker.

```bash
git clone https://github.com/AbhishekThite387/full-stack_chatApp.git
```

```bash
cd full-stack_chatApp
```

## Create a Docker network:

```bash
docker network create full-stack
```

## 🛠️ Building the Frontend

```bash
cd frontend
```

```bash
docker build -t full-stack_frontend .
```

### Run the Frontend container:

```bash
docker run -d --network=full-stack  -p 5173:5173 --name frontend full-stack_frontend:latest
```

#### The frontend will now be accessible on port 5173.

### Run the MongoDB Container:

```bash
docker run -d -p 27017:27017 --name mongo mongo:latest
```

---

## 🛠️ Building the Backend

```bash
cd backend
```

### Build the Backend image:

```bash
docker build -t full-stack_backend .
```

### Run the Backend container:

```bash
docker run -d --network=full-stack --add-host=host.docker.internal:host-gateway -p 5001:5001 --env-file .env full-stack_backend

```

#### This will build and run the backend container, exposing the backendAPI on port 5001.

`Backend API: http://localhost:5001`

### To Verify the conncetion between backend and databse:

```bash
docker-compose logs -f
```

### Once the backend and frontend containers are running, you can access the application in your browser:

`Frontend: http://localhost`

You can now interact with the real-time chat app and start messaging!

---

# 📸 Project Screenshots

## 🔐 Login Page

![Login](frontend/public/my-login.png)

---

## 💬 Chat Interface

![Chat](frontend/public/my-chat.png)

---

## 👤 Profile Page

![Profile](frontend/public/profile-page.png)

---

## ⚙️ Settings Page

![Settings](frontend/public/settings-page.png)

## 📜 License

This project is licensed under the MIT License. See the LICENSE file for more details.

# ⭐ Support

If you like this project, please give it a ⭐ on GitHub.

---

# 👨‍💻 Author

Developed by Abhishek 🚀
