# Rhombixtechnologies_Task-2
 Flask Docker Project

A simple Flask web application containerized using Docker. This project demonstrates how to build, package, and run a Python Flask app inside a Docker container.

 Project Overview

This project contains a basic Flask application that returns a simple message:

Hello, Docker Project!

The app is fully containerized using Docker, making it portable and easy to deploy on any system.

🚀 Features
Simple Flask web app
Dockerized environment
Easy build & run setup
Portable across systems
Beginner-friendly DevOps project
 Project Structure
docker_project/
│
├── app.py               # Flask application
├── requirements.txt     # Python dependencies
├── Dockerfile           # Docker configuration
└── README.md            # Project documentation
 Prerequisites

Make sure you have installed:

Docker Desktop → https://www.docker.com/
Python (optional for local testing)
Git (optional)

Check Docker version:

docker --version
🧑‍💻 Setup & Installation
1️⃣ Clone the repository
git clone https://github.com/EliteZain657/Rhombixtechnologies_Task-2.git
cd docker-flask-project
2️⃣ Build Docker Image
docker build -t flask-docker-app .
3️⃣ Run Docker Container
docker run -p 5000:5000 flask-docker-app
4️⃣ Open in Browser
http://localhost:5000
📦 Dockerfile Explanation
FROM python:3.9

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt

COPY . .

CMD ["python", "app.py"]
What it does:
Uses Python base image
Sets working directory
Installs dependencies
Copies project files
Runs Flask app
 requirements.txt
flask
 app.py
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello, Docker Project!"

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=5000)
 Useful Docker Commands
docker ps          # running containers
docker ps -a       # all containers
docker stop <id>   # stop container
docker rm <id>     # remove container
docker images      # list images
 Learning Outcome

After completing this project, you will understand:

Basics of Docker
Containerizing Python applications
Building Docker images
Running containers
Port mapping concept
📌 Future Improvements
Add Docker Compose
Connect database (MySQL/PostgreSQL)
Deploy on cloud (AWS / Render / Railway)
Add frontend UI
