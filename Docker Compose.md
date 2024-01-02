Lab 10: Docker Compose 
-------------------------------------------------------------
Task 1:
-------------------------------------------------------------

# wget https://bootstrap.pypa.io/pip/2.7/get-pip.py
# apt install python3 -y
# python3 get-pip.py
# pip3 install docker-compose

-------------------------------------------------------------
Task 2: Create a docker-compose.yaml for Wordpress application
-------------------------------------------------------------
# mkdir wordpress
# cd wordpress

vi docker-compose.yaml

version: '3.3'

services:
  db:
    image: mysql:5.7
    volumes:
      - db_data:/var/lib/mysql
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: somewordpress
      MYSQL_DATABASE: wordpress
      MYSQL_USER: wordpress
      MYSQL_PASSWORD: wordpress

  wordpress:
    depends_on:
      - db
    image: wordpress:latest
    ports:
      - "80:80"
    restart: always
    environment:
      WORDPRESS_DB_HOST: db:3306
      WORDPRESS_DB_USER: wordpress
      WORDPRESS_DB_PASSWORD: wordpress
      WORDPRESS_DB_NAME: wordpress
volumes:
  db_data: {}


docker-compose up -d

docker-compose ps

docker container ls
docker network ls
docker volume ls

docker-compose down
