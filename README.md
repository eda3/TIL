# Docker

docker pull ubuntu

docker run --name=httpd_temp rhel7:latest /bin/bash -c "yum install httpd -y;"

docker run -it --name ubuntu ubuntup

docker login -e

### イメージ一覧
docker images

### 起動してすぐログイン
docker run -it ccc6e87d482b bash


# Linux

sudo apt-get install build-essential curl git m4 ruby texinfo libbz2-dev libcurl4-openssl-dev libexpat-dev libncurses-dev zlib1g-dev

sudo apt-get install build-essential curl file git

sudo apt install -y xclip
sudo apt install -y ansible


## Gentoo Linux
### Change to root user
sudo su

### Make ssh key
sh-keygen -t rsa

useradd user -m -G users,wheel,tty -s /bin/bash
passwd user

### ssh

vi /etc/ssh/sshd_config
( Port 22 )
( Protocol 2 )

/etc/init.d/sshd start

### Docker
sudo emerge -av app-emulation/docker

groupadd docker

sudo usermod -a -G docker user

/etc/init.d/docker start

rc-update add docker default

systemctl start docker

systemctl enable docker