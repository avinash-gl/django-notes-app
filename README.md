
# 📝 Django Notes App (3-Tier Dockerized Deployment)

A simple **Django-based Notes Application** that allows users to create, read, update, and delete notes. This project is structured using a **3-tier architecture** with:

- **Web Server:** NGINX
- **App:** Django (Python)
- **Database:** MySQL  
All components are containerized using **Docker Compose**.


## Features

- **Persistent Volumes:**  
  Data is retained even if containers stop or restart.

- **Shared Docker Network:**  
  All containers run on the same custom Docker network to enable internal communication.

- **Reverse Proxy via NGINX:**  
  NGINX routes incoming HTTP requests to the Django backend securely without exposing the application port.

- **Modular Configuration:**  
  NGINX Dockerfile and configuration files are placed inside the `/nginx` directory for easy customization.



## Usage

1. Clone the Repository.
```bash
git clone https://github.com/avinash-gl/docker-projects.git
cd projects/3-tier-notes-app
```

2. Run the containers
```bash
docker compose up --build
```

3. In your browser, visit `http://localhost:80` if the app is running.


