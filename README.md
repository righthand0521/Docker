# [Docker](https://zh.wikipedia.org/wiki/Docker)

## [Install Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/)

```bash
apt install docker.io -y

service --status-all
update-rc.d docker enable
service docker start
service docker status
```

```bash
ls -l /var/lib/docker/

docker version
docker info

docker search
docker pull

docker images
docker rmi

docker inspect <IMAGE ID>
docker history <IMAGE ID>
docker history --no-trunc <IMAGE ID>

docker ps -a
docker stop $(docker ps -q)
for i in $(docker ps -q -f status=exited); do docker rm -f $i; done

docker run
```

## docker-compose.yml

```bash
docker-compose version
docker-compose up -d
docker-compose down
docker-compose ps
docker-compose logs
```

## docker build

```bash
docker build --tag <tag> -f <Dockerfile File> .
docker build --tag test .

docker run test
docker run --rm -it test bash
```
