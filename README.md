                 |

## 📦 Docker Containerization

This project is fully containerized using **Docker**. The Dockerfile sets up the Node.js environment and prepares the API for production use.

### 🔧 Build Docker Image

```bash
docker build -t ec2-api-project .
```

### ▶️ Run Container Locally

```bash
docker run -p 5000:5000 ec2-api-project
```

Test endpoints:

- `http://localhost:5000/students`
- `http://localhost:5000/subjects`

---

## 🧩 Docker Compose Setup

We use **Docker Compose** to run the API alongside a PostgreSQL container.

### 📄 docker-compose.yml

This file defines:

- `api` container (Node.js)
- `postgres` container (PostgreSQL)
- Networking, volumes, environment variables

### ▶️ Run with Compose

```bash
docker compose up --build
```

To stop:

```bash
docker compose down
```

---

## ☁️ Docker Deployment on AWS EC2

On your EC2 Ubuntu instance:

1. Install Docker and Docker Compose
2. Clone this repo
3. Run:

```bash
docker compose up -d
```

Your app is now containerized and publicly accessible.

---

## 🐳 Docker Hub Image

The API Docker image is available on Docker Hub:

🔗 **[https://hub.docker.com/r/ceolayson/udom-api](https://hub.docker.com/r/ceolayson/udom-api)**

Pull with:

```bash
docker pull ceolayson/udom-api
```

---

## 📷 Docker Logs & Screenshot

- `docker_ps.png`: Shows running containers using `docker ps`
- `docker_logs.txt`: Contains output logs from your Docker containers

> **Author:** CEO-LAYSON | University of Dodoma | CS421 – Application Deployment and Management

## 🚀 How to Build Docker Image

docker build -t ec2-docker-project-api .

## 🐳 How to Run with Docker Compose

docker compose up --build

## 📦 Docker Hub Link

https://hub.docker.com/r/crntechnologies/udom-api

## 🧯 Troubleshooting

- If containers fail, check logs: `docker logs container_id`
- Ensure PostgreSQL container is running
- Ensure ports (5000) are exposed and available

> **Author:** CEO-LAYSON | University of Dodoma | CS421 – Application Deployment and Management
