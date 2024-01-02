## Basic Docker Commands

### Task 1: Creating your first Docker container

```
docker run hello-world
```
### Task 2: Basic Commands to run the Container in Interactive mode

```
docker pull ubuntu
```
```
docker image ls
```
```
docker run -it --name ct1 ubuntu
```
```
touch f1 f2 f3
```
```
ls
```
```
exit
```
```
docker ps
```
```
docker ps -a
```
```
docker run -it --name ct2 ubuntu
```
Press Crtl+P+Q to switch the terminal to Docker Host.
```
docker ps
```
```
docker exec -it ct2 /bin/sh
```
```
exit
```
```
docker ps
```
```
docker attach ct2
```
```
exit
```
```
docker ps
```
```
docker ps -a
```

### Task 3: Port Mapping from Docker Host to container
```
docker run -d -p 80:80 httpd
```
```
docker ps
```
```
docker exec -it < replace container id/name > /bin/bash
```
```
exit
```
```
docker ps
```
```
docker exec -it < replace container id/name > /bin/bash
```
```
kill 1
```
```
docker ps -a
```
```
docker container stop < replace container id/name >
```
```
docker container rm < replace container id/name >
```
```
docker image ls
```
```
docker image rm < replace image id >
```
