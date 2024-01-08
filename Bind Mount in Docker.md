## Bind Mount in Docker

### Task 1: Starting Docker Containers Bind Mounts
```
mkdir /home/ubuntu/share
```
```
echo 'Hello From Docker Host' > /home/ubuntu/share/index.html
```
```
docker run -it --name container1 -p 80:80 -v /home/ubuntu/share:/var/www/html ubuntu:18.04 /bin/bash
```
```
apt-get update -y && apt-get install apache2 -y
```
```
service apache2 start
```
```
service apache2 status
```
```
echo 'Hello From Container1' > /var/www/html/index.html
```

Press Ctrl+P+Q, to switch back to Host
```
docker run -it --name container2 -v /home/ubuntu/share:/var/www/html ubuntu:18.04
```
```
echo 'Hello From Container2' > /var/www/html/index.html 
```
```
exit
```
```
docker ps -a
```
```
docker rm -vf container1 container2 
```

### Task 2: Create a bind mount with --mount option and verify it
```
docker run -d -it --name newbind01 --mount type=bind,source=/home/ubuntu/share/,target=/app nginx:latest
```
```
docker inspect newbind01
```
```
docker exec -it newbind01 bash
```
```
mount | grep -i /app
```
