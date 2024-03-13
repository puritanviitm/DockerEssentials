## Pushing the image to DockerHub
```
docker login
```
```
docker pull ubuntu
```
Make sure to replace `meharnafisdockerhub` with the name of your DockerHub repo
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
docker ps -a
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

