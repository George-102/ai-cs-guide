# Docker

## 为什么使用 Docker

在学习 CS 课程的过程中，你经常会遇到这样的问题：

- 课程实验要求特定的操作系统或软件版本
- 本地环境和老师提供的环境不一致，导致代码运行结果不同
- 安装一个软件需要配置大量依赖，过程繁琐且容易出错

Docker 通过容器化技术解决了这些问题。容器就像一个轻量级的虚拟机，它把你的程序和它需要的所有依赖打包在一起，在任何地方都能以相同的方式运行。

**环境一致性，一次构建到处运行**

Docker 容器封装了完整的运行环境，包括操作系统、库和依赖。你本地能跑的代码，放到服务器上、别人电脑上也能跑，彻底告别"在我电脑上能跑"的问题。

**快速部署，秒级启动**

相比传统虚拟机需要几分钟启动，Docker 容器可以在几秒内启动，资源占用也更少。

**CS 课程实验利器**

很多 CS 课程（如操作系统、数据库、网络）的实验都提供 Docker 镜像，直接拉取即可使用，免去繁琐的环境配置。

## 安装 Docker

**Windows**

推荐使用 [Docker Desktop for Windows](https://docs.docker.com/desktop/install/windows-install/)。

> 注意：Docker Desktop 需要开启 WSL2 或 Hyper-V。如果你使用 WSL2（推荐），Docker 会自动利用 WSL2 的 Linux 内核。

**macOS**

下载 [Docker Desktop for Mac](https://docs.docker.com/desktop/install/mac-install/)。

**Linux**

```bash
# Ubuntu
sudo apt update
sudo apt install docker.io
sudo systemctl start docker
sudo systemctl enable docker
# 将当前用户加入 docker 组（免 sudo）
sudo usermod -aG docker $USER
```

## 基本使用

**拉取并运行镜像**

```bash
# 拉取一个 Ubuntu 镜像
docker pull ubuntu

# 运行一个容器
docker run -it ubuntu bash

# 运行一个 Python 容器
docker run -it python:3.11 bash
```

**常用命令**

```bash
docker ps                        # 查看正在运行的容器
docker ps -a                     # 查看所有容器（包括已停止的）
docker stop <container_id>       # 停止容器
docker rm <container_id>         # 删除容器
docker images                    # 查看本地镜像
docker rmi <image_id>            # 删除镜像
```

**使用 Dockerfile**

Dockerfile 是一个文本文件，描述了如何构建镜像：

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

**挂载本地目录**

将本地代码目录挂载到容器中，方便开发调试：

```bash
docker run -v $(pwd):/app -w /app -it python:3.11 bash
```

## Docker Compose

当你的应用需要多个服务（如 Web 服务器 + 数据库）时，Docker Compose 可以帮你一次性启动和管理多个容器：

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
docker compose up -d      # 启动所有服务
docker compose down       # 停止所有服务
```

## 其他资源

- [Docker 官方文档](https://docs.docker.com/)
- [Docker — 从入门到实践](https://yeasy.gitbook.io/docker_practice/)
- [Play with Docker](https://labs.play-with-docker.com/) — 在线体验 Docker
