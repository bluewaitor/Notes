# Docker 基础

## Docker 是什么？

`Docker`

## Docker 安装

- `brew cask install docker`
- `docker --version` 查看 Docker 版本
- `docker version` 可以查看客户端和服务端的信息
- `docker info` 可以查看更详细的信息

## 测试Docker安装是否成功

运行`docker run hello-world`这条命令，如果出现以下的结果，则说明安装成功。

```bash
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
d1725b59e92d: Pull complete
Digest: sha256:0add3ace90ecb4adbf7777e9aacf18357296e799f81cabc9fde470971e499788
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```

## 查看帮助

`docker` 或者 `docker --help` 显示帮助
`docker <COMMAND> --help` 显示命令COMMAND的帮助信息, 比如`docker container --help` 显示容器命令的帮助信息

## Docker Image

`Docker镜像` 可以理解为面向对象中的 `类`

`docker pull <IMAGE_NAME>` 拉取(下载)一个 Docker 镜像

`docker images` 或者 `docker image ls` 列出 Docker 镜像

## Docker Container

`Docker容器` 相当于面向对象中的`对象`

`docker container ls` 列出正在运行的 Docker 容器

`docker container ls -a` 列出所有的 Docker 容器，包括已经停止的容器

## 执行Docker镜像

`docker run <IMAGE_NAME>`

主要参数：

- `-d` detach分离模式，相当于后台运行
- `-i` interactive交互模式
- `-t` tty

## 删除没用的镜像

`docker rmi $(docker images -f "dangling=true" -q)`

## 命令行提醒（for zsh）

```bash
etc=/Applications/Docker.app/Contents/Resources/etc
ln -s $etc/docker.zsh-completion /usr/local/share/zsh/site-functions/_docker
ln -s $etc/docker-machine.zsh-completion /usr/local/share/zsh/site-functions/_docker-machine
ln -s $etc/docker-compose.zsh-completion /usr/local/share/zsh/site-functions/_docker-compose
```
