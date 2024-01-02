## Creating an EC2 Instance in AWS and Installing Docker

To begin, log in to AWS Console.

### Task-1:  Launching EC2 instances and Connecting to EC2 Instances using SSH

* Manually Launch a `t2.micro` instance with OS version as `Ubuntu 22.04 LTS` in North Virginia (us-east-1) Region.
* Enable `SSH`, `HTTP`, `HTTPS` and `Port no. 8080`.
* Configure Storage: `10 GiB`
* Once Launched, Connect to the Instance using `MobaXterm` or `Putty` or `EC2 Instance Connect` with username "`ubuntu`".

### Task-2: Installing Docker on Ubuntu 18.04 operating system 
```
sudo hostnamectl set-hostname docker
```
```
bash
``` 
```
sudo su
```
```
apt update -y
```
```
apt install curl -y
```
```
curl -SSL https://get.docker.com/ | sh
```
```
service docker status   # systemctl status docker
```
To add ubuntu user to doccker group
```
usermod -aG docker ubuntu
```
```
docker --version
```
