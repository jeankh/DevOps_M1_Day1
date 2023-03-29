
# Tuto Docker

```bash
docker search Hello-world
docker pull hello-world
docker run --name "hello_v1" hello-world

docker search nginx
docker pull nginx
docker run --name "nginx_n1" -d -p 8080:80 nginx
docker run --name "nginx_n2" -d -p 8081:80 nginx
```

```bash
docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS                                   NAMES
3b4bd871dcf1   nginx     "/docker-entrypoint.…"   12 seconds ago   Up 11 seconds   0.0.0.0:8081->80/tcp, :::8081->80/tcp   nginx_n2
d422e9d4fbdf   nginx     "/docker-entrypoint.…"   23 minutes ago   Up 23 minutes   0.0.0.0:8080->80/tcp, :::8080->80/tcp   nginx_n1
```

```bash
mkdir DevOps
cd DevOps/
touch Dockerfile
nano Dockerfile
```

```docker
FROM alpine:3.16.4

CMD echo "coucouc from jean"
```

```bash
docker build -t jeankh/coucou .
docker run --name "coucou" jeankh/coucou
docker push jeankh/coucou
```
