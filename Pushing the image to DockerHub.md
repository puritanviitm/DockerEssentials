## Pushing the image to DockerHub
```
docker login
```
```
docker pull ubuntu
```
```
docker tag ubuntu:latest meharnafisdockerhub/ubuntu:mehar
```
```
docker image ls
```
```
docker push meharnafisdockerhub/ubuntu:mehar
```
```
docker image ls
```
```
docker image rm meharnafisdockerhub/ubuntu:mehar   #local repo
```
```
docker run -d -p 8080:80 meharnafisdockerhub/ubuntu:mehar
```
```
docker stop < replace container id/name >
```
```
docker container rm < replace container id/name >
```
```
docker image ls
```
```
docker image rm < replace image id/name > < replace image id/name >
```
```
docker image ls
```
```
docker image ls -a
```
