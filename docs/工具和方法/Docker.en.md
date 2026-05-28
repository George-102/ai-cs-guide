# Docker

## Why use Docker

While studying CS courses, you often encounter these problems:

- Course labs require specific operating systems or software versions
- Your local environment differs from the instructor's, causing different results
- Installing software requires configuring many dependencies — tedious and error-prone

Docker solves these problems through containerization. Containers are like lightweight virtual machines that package your program with all its dependencies, ensuring it runs the same way everywhere.

**Environment consistency, build once run anywhere**

Docker containers encapsulate the complete runtime environment, including the OS, libraries, and dependencies. Code that runs locally will also run on servers and other people's machines. Say goodbye to "it works on my machine."

**Fast deployment, instant startup**

Compared to traditional virtual machines that take minutes to boot, Docker containers start in seconds and use fewer resources.

**Essential for CS course labs**

Many CS courses (operating systems, databases, networking) provide Docker images. Just pull and use — no more tedious environment setup.

## Installing Docker

**Windows**

Recommended: [Docker Desktop for Windows](https://docs.docker.com/desktop/install/windows-install/).

> Note: Docker Desktop requires WSL2 or Hyper-V. If you use WSL2 (recommended), Docker will automatically leverage the WSL2 Linux kernel.

**macOS**

Download [Docker Desktop for Mac](https://docs.docker.com/desktop/install/mac-install/).

**Linux**

```bash
# Ubuntu
sudo apt update
sudo apt install docker.io
sudo systemctl start docker
sudo systemctl enable docker
# Add current user to docker group (avoid sudo)
sudo usermod -aG docker $USER
```

## Basic usage

**Pull and run images**

```bash
# Pull an Ubuntu image
docker pull ubuntu

# Run a container
docker run -it ubuntu bash

# Run a Python container
docker run -it python:3.11 bash
```

**Common commands**

```bash
docker ps                        # View running containers
docker ps -a                     # View all containers (including stopped)
docker stop <container_id>       # Stop a container
docker rm <container_id>         # Remove a container
docker images                    # View local images
docker rmi <image_id>            # Remove an image
```

**Using Dockerfile**

A Dockerfile is a text file that describes how to build an image:

```dockerfile
FROM python:3.11
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
CMD ["python", "main.py"]
```

```bash
docker build -t myapp .
docker run -it myapp
```

**Mounting local directories**

Mount your local code directory into the container for easy development and debugging:

```bash
docker run -v $(pwd):/app -w /app -it python:3.11 bash
```

## Docker Compose

When your application needs multiple services (e.g., web server + database), Docker Compose lets you start and manage multiple containers at once:

```yaml
# docker-compose.yml
services:
  web:
    build: .
    ports:
      - "8000:8000"
  db:
    image: postgres:15
    environment:
      POSTGRES_PASSWORD: example
```

```bash
docker compose up -d      # Start all services
docker compose down       # Stop all services
```

## Other resources

- [Docker Official Documentation](https://docs.docker.com/)
- [Docker — From Beginners to Pros](https://yeasy.gitbook.io/docker_practice/)
- [Play with Docker](https://labs.play-with-docker.com/) — Try Docker online
