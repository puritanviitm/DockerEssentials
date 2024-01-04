## Docker container life cycle

### Task 1: Docker Lifecycle 
Pull Docker Image
```
docker pull httpd
```
List all images available in Local Repo
```
docker image ls
```
Check the history of the image
```
docker image history httpd
```
Create container
```
docker container create httpd
```
List all containers
```
docker container ls -a
```
```
docker container start < container id/name >
```
```
docker container ls
```
```
docker container stop < replace container id/Name >
```
```
docker container ls -a
```
```
docker container start < replace container id/Name >
```
```
docker container pause < replace container id/Name >
```
```
docker container ls -a
```
```
docker container unpause < replace container id/Name >
```
```
docker container ls -a
```
```
docker exec -it < replace container id/name > bash
```
```
cd htdocs
```
```
apt update
```
```
apt install wget -y
```
```
rm index.html
```
```
wget https://s3.ap-south-1.amazonaws.com/files.cloudthat.training/devops/docker-essentials/index.html
```
```
exit
```
```
docker commit < replace container id/name > myhttpd:version
```
```
docker image ls
```
```
docker run -d -p 8080:80 myhttpd:version
```
```
curl < public IP>:8080
```
```
docker container ls
```
```
docker logs < replace container id/name >
```
```
docker stats < replace container id/name >
```
```
docker container ls
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
