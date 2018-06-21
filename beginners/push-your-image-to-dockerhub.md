
# How to push your First Image to Dockerhub

## Pull Ubuntu Image from Dockerhub

```
$docker pull ubuntu
```

## Running Ubuntu Container

```
$docker run -itd ubuntu /bin/bash
```

## Enter into Container Shell

```
$docker attach <container-id>
```

## Install software(networking tool) inside Docker container

```
$apt update && apt install net-tools
```

## Exiting the container shell without stopping the container

Press Ctrl + P + Q at the same time


## Commiting the Docker Image

```
$docker commit -m "Added Networking tool" <containerid>
```

## Tagging the Docker Image

```
$ docker tag net-tools collabnixlabs/ubuntu-nettools:v1.0
```


## Listing the Images

```
[node1] (local) root@192.168.0.48 ~
$ docker images
REPOSITORY                      TAG                 IMAGE ID            CREATED             SIZE
collabnixlabs/ubuntu-nettools   v1.0                12ff85226c56        59 seconds ago      123MB
net-tools                       latest              12ff85226c56        59 seconds ago      123MB
ubuntu-nettools                 v1.0                12ff85226c56        59 seconds ago      123MB
ubuntu                          latest              113a43faa138        2 weeks ago         81.2MB
[node1] (local) root@192.168.0.48 ~
```

```
$ docker push collabnixlabs/ubuntu-nettools:v1.0
The push refers to repository [docker.io/collabnixlabs/ubuntu-nettools]
668bf781af1a: Pushed
b6f13d447e00: Pushed
a20a262b87bd: Pushed
904d60939c36: Pushed
3a89e0d8654e: Pushed
db9476e6d963: Pushed
v1.0: digest: sha256:281e6c10d36db7bb24aef4845487fc4bb900987644224c873badf4b017e8dea4 size: 1569
[node1] (local) root@192.168.0.48 ~
$
```
