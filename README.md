# docker-envionment
A basic docker development environment with a network, redis container and a reverse proxy

# Setup
Before building the environment for the first time, you must first create the volumes and network used by the included containers

## Create the network

```console
docker network create environment --subnet=172.18.0.0/16
```

## Create the volumes

```console
docker volume create cache
docker volume create logs
docker volume create redis
```

## Build the environment
```console
make docker-build-from-scratch
```
