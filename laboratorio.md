
## Descarga imagen ubuntu 

@gokev06 ➜ /workspaces/labs-docker-dev (main) $ docker pull ubuntu
Using default tag: latest
latest: Pulling from library/ubuntu
9c704ecd0c69: Pull complete 
Digest: sha256:2e863c44b718727c860746568e1d54afd13b2fa71b160f5cd9058fc436217b30
Status: Downloaded newer image for ubuntu:latest
docker.io/library/ubuntu:latest



## Descarga imagen python:3.9

@gokev06 ➜ /workspaces/labs-docker-dev (main) $ docker pull python:3.9
3.9: Pulling from library/python
ca4e5d672725: Pull complete 
30b93c12a9c9: Pull complete 
10d643a5fa82: Pull complete 
d6dc1019d793: Pull complete 
c387064957b7: Pull complete 
26766ebde481: Pull complete 
8a42d17fd0e2: Pull complete 
79eda865cc8a: Pull complete 
Digest: sha256:fea84f3a3b72c41efe7fc3b07ae209c6856b852b942c05fa88b747b74f70e711
Status: Downloaded newer image for python:3.9
docker.io/library/python:3.9
@gokev06 ➜ /workspaces/labs-docker-dev (main) $ 

## Ejecutar contenedor

@gokev06 ➜ /workspaces/labs-docker-dev (main) $ docker run -it ubuntu bash
root@424b53bf064a:/#

## Eliminar contenedores

@gokev06 ➜ /workspaces/labs-docker-dev (main) $ docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED      STATUS                        PORTS                                   NAMES
424b53bf064a   ubuntu    "bash"                   4 days ago   Exited (255) 15 minutes ago                                           busy_carson
e25b08415456   nginx     "/docker-entrypoint.…"   4 days ago   Exited (255) 15 minutes ago   0.0.0.0:8080->80/tcp, :::8080->80/tcp   dazzling_keldysh
@gokev06 ➜ /workspaces/labs-docker-dev (main) $ docker rm 424b53bf064a
424b53bf064a
@gokev06 ➜ /workspaces/labs-docker-dev (main) $ docker rm 424b53bf064a
Error response from daemon: No such container: 424b53bf064a
@gokev06 ➜ /workspaces/labs-docker-dev (main) $ docker container prune
WARNING! This will remove all stopped containers.
Are you sure you want to continue? [y/N] y
Deleted Containers:
e25b0841545665d2187dbce5bcc6138796e8cf19f1a85cb181ac4faca8aec3c8

Total reclaimed space: 1.095kB