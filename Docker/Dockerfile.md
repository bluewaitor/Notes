# Dockerfile

我们可以通过创建`Dockerfile`来创建镜像

```Dockerfile
FROM alpine
RUN apk update && apk add nodejs
COPY . /app
WORKDIR /app
CMD ["node", "index.js"]
```

- `FROM` 基于哪个镜像
- `RUN` 执行命令
- `COPY` 将当前目录的内容拷贝到容器的`/app`目录下
- `WORKDIR` 工作目录，相当于`cd /app`
- `CMD` 每次container启动执行的命令
  
`docker [container] commit <CONTAINER_ID>` 提交容器的改变使其成为一个镜像

`docker [image] build -t <TAG_NAME>:<VERSION>` 构建镜像

`docker [image] history <IMAGE_ID>` 查看镜像的历史

`docker [image] inspect <IMAGE_ID|IMAGE_NAME>` 查看镜像信息