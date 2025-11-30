# Docker Setup for WordPress

This project provides a fully containerized WordPress environment using Docker and Docker Compose.
It includes both the WordPress application and a MariaDB database, making it easy to run your own blog locally or on a remote server.
The setup is ideal for development, testing, or learning how to deploy WordPress in a modern DevOps environment.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Quickstart](#-quickstart)
3. [Usage](#-usage)
   - [Create a Docker Container](#-create-a-docker-container)
   - [Docker Management Commands](#docker-compose-commands)
4. [Project Checklist](#project-checklist)

## Prerequisites

Before you begin, ensure that the following are installed and set up on your local machine or server:
- [Docker](https://docs.docker.com/get-docker/)

Info: Docker Compose is automatically included in Docker Desktop and Docker Engine.

## 🚀 Quickstart

Clone this repository and follow the setup instructions below to get the application running.

Open your command line and type the following commands:
With SSH configured (if SSH Keys are provided to GitHub)
```
git clone git@github.com:MWorksCoding/wordpress-docker.git
```
Classic HTTPS (if no SSH Keys are provided to GitHub)
```
git clone https://github.com/MWorksCoding/wordpress-docker.git
```

Navigate to the root project directory you just cloned.
```
cd wordpress-docker
```
> [!NOTE]
> Inside your project root directory, you need to create a `.env` file for your environment variables.  
> You can copy and paste the content from [example.env](./example.env) by running:
>
> ```
> cp example.env .env
> ```
>
> Please keep in mind that the values should only be used for local development for security reasons.

Docker Compose automatically loads .env files, so you don’t need to reference it manually.

From here, you can build the Docker container and start the server with Docker Compose:
```
docker compose build --no-cache
```

```
docker compose up
```

You can check our your localhost at port 8080:
```
http://localhost:8080
```

Or if running on a server with a public IP:
```
http://<your-ip>:8080
```

You should now see the WordPress installation page.  
After accessing the site, you must complete the WordPress setup by selecting a site title, creating an admin account, and configuring your preferred settings.

Please check the list of typical Docker commands in the section [Docker Management Commands](#docker-compose-commands)

## 🧑‍💻 Usage

### 🐳 Create a Docker Container

General Informations:

That [docker-compose.yml](./docker-compose.yaml) file tells Docker exactly how to build, run, configure, and manage your project — all in one place.

### Docker Compose Commands

| Command | Description |
|--------|-------------|
| `docker compose build` | Build the Docker image according to your Dockerfile. |
| `docker compose build --no-cache` | Build from scratch without using cached layers. |
| `docker compose up` | Start the container in the foreground (logs visible). |
| `docker compose up -d` | Start the container in detached/background mode. |
| `docker compose up --build` | Build and start containers at the same time. |
| `docker compose up --build -d` | Build and start containers in detached mode. |
| `docker compose stop` | Stop running containers without removing them. |
| `docker compose restart` | Restart all running services. |
| `docker compose down` | Stop and remove containers, networks, and volumes. |
| `docker compose logs -f` | Follow logs in real time. |
| `docker compose logs` | Show logs without following. |
| `docker exec -it minecraft-server /bin/sh` | Open an interactive shell inside the running container. |
| `docker compose ps` | List running containers. |

## Project Checklist

You can find a detailed checklist for this project in PDF format:

- [Download the Checklist](../wordpress-docker/docs/checklist.pdf)