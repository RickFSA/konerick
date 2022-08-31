# DOCKER (Linux and MacOS)

[Documentation](https://www.docker.com/)

### View running docker container
```shell
docker ps
```

### View all docker container
```shell
docker ps -a
```

### View docker images
```shell
docker images
```

### View docker network
```shell
docker network ls
```

### Pull an image from DockerHub
```shell
docker pull <IMAGE_NAME>
```

### Remove an image
```shell
docker rmi <IMAGE_ID>
```

### Remove a container
```shell
docker rm <CONTAINER_ID>
```

### Build a docker container
```shell
docker run -it <IMAGE_NAME>:<tag> -d
```
`-it`: interactive mode
`-d`: detach mode

### Build a Postgres container (EXAMPLE)
```shell
docker run -it \
 -e POSTGRES_USER="user" \
 -e POSTGRES_PASSWORD="password" \
 -v <PATH>:/var/lib/postgresql/data \
 -p 5432:5432 \
 --name postgres-database \
postgres:13 
```
`-e`: parameters
`-v`: volumns
`-p`: ports
`--name`: container name

### Stop a container
```shell
docker stop <CONTAINER_NAME>
```

### Start a container
```shell
docker start <CONTAINER_NAME>
```

### Build a docker image
```shell
docker build -t <IMAGE_NAME>:<tag> .
```
build an image from a Dockerfile

### Run a docker-compose.yaml file
```shell
docker-compose up -d
```
Run a docker-compose on a docker-compose.yaml file located under the same directory

### Shutdown a docker-compose
```shell
docker-compose down
```
