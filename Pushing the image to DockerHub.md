Lab 8: Pushing the image to DockerHub
-------------------------------------------------------------
docker login
docker tag ct-wordpress:v1 <replace your dockerhub account name>/ct-wordpress:v1
docker image ls

docker push <replace your dockerhub account name>/ct-wordpress:v1

docker image ls
docker image rm <replace your dockerhub account name>/ct-wordpress:v1 ct-wordpress:v1   #local repo
docker run -d -p 8080:80 <replace your dockerhub account name>/ct-wordpress:v1
docker stop < replace container id/name >
docker container rm < replace container id/name >
docker image ls
docker image rm < replace image id/name > < replace image id/name >
docker image ls
docker image ls -a
