# Full-Stack User Management App

This project is a **full-stack web application** that demonstrates CRUD operations (Create, Read, Update, Delete) on user data using a **React + Next.js frontend** and a **Flask backend** connected to a **PostgreSQL database**. It is containerized with **Docker Compose** for seamless deployment.

## 🧩 Overview

The frontend, built with React and TypeScript, provides an intuitive interface for managing users — displaying user cards, adding new users, updating existing ones, and deleting entries. The backend, powered by Flask, exposes RESTful API endpoints to interact with the PostgreSQL database. Docker Compose coordinates the three core services: the frontend, Flask API, and PostgreSQL.

## ⚙️ Tech Stack

* **Frontend:** React, Next.js, TypeScript, Axios, TailwindCSS
* **Backend:** Flask (Python)
* **Database:** PostgreSQL
* **Deployment:** Docker, Docker Compose

## 🧠 How It Works

* The **Flask API** (port `4000`) handles requests like `/api/flask/users` for user operations.
* The **React/Next.js UI** consumes this API to dynamically display user data and perform CRUD actions.
* The **PostgreSQL service** stores all user records persistently through Docker volumes.
* Configuration is managed in `compose.yml`, which defines services for Flask and the database.


Here’s an updated **README.md** section you can append after the overview:

---

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd <your-repo-name>
```

### 2. Build and Run with Docker Compose

Make sure Docker is installed and running, then execute:

```bash
docker compose up --build
```

This command will:

* Build the Flask image using `flask.dockerfile`
* Start the Flask backend on **port 4000**
* Launch a **PostgreSQL** database on **port 5432**
* Persist database data through a Docker volume (`pgdata`)

### 3. Access the Application

Once the containers are running:

* **Frontend:** [http://localhost:3000](http://localhost:3000)
* **Backend API:** [http://localhost:4000/api/flask/users](http://localhost:4000/api/flask/users)
* **Database:** localhost:5432 (user: `postgres`, password: `postgres`)

### 4. Stopping the Containers

```bash
docker compose down
```

To also remove volumes (clears all stored data):

```bash
docker compose down -v
```

---
