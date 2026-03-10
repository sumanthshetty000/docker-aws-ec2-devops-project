# Dockerized Web Application Deployment on AWS EC2

## Project Overview
This project demonstrates how to deploy a containerized web application using Docker on an AWS EC2 instance.

The application is served using Nginx inside a Docker container and exposed to the internet through port mapping.

---

## Architecture

User → Internet → AWS EC2 → Docker Container → Nginx → Web Application

---

## Technologies Used

- Linux (Ubuntu)
- Docker
- AWS EC2
- Nginx
- Git & GitHub

---

## Project Setup

### Launch EC2
- Ubuntu 22.04
- Open ports:
  - 22 (SSH)
  - 8080 (Application)

### Install Docker

```bash
sudo apt update
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
```

### Build Docker Image

```bash
docker build -t devops-web .
```

### Run Container

```bash
docker run -d -p 8080:80 devops-web
```

Access application:

```
http://<EC2-PUBLIC-IP>:8080
```

---

## Project Screenshot
![Project Screenshot](Project-output.png)

---

## Key DevOps Concepts Practiced

- Docker image creation
- Container deployment
- Port mapping
- AWS EC2 server management
- Security group configuration
- Linux server administation

---

## Author

Sumanth  
Aspiring DevOps Engineer
