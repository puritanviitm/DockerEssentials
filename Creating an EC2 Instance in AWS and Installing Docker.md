-------------------------------------------------------------
Task 1: Launching EC2 instances  
-------------------------------------------------------------
t2.micro
Ubuntu Server 18.04 LTS (HVM) Free tier eligible
10 gb hdd
enable SSH, HTTP, HTTPS and port no. 8080


-------------------------------------------------------
Task 2: Connecting to EC2 Instances using SSH
-------------------------------------------------------------
*Open PuTTY software
*In PuTTY Configuration window, Paste your EC2 Public IP or Public DNS in the Hostname (or IP Address) field, select Private Key and Now click on Open

-------------------------------------------------------------
Task 3: Installing Docker on Ubuntu 18.04 operating system 
------------------------------------------------------------
sudo hostnamectl set-hostname docker

logout and relogin 
sudo su
apt update -y
apt install curl -y

curl -SSL https://get.docker.com/ | sh

service docker status   # systemctl status docker

usermod -aG docker ubuntu
#regular user --ubuntu---ubuntu user into docker group

docker --version
