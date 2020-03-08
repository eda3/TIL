# Docker

docker pull ubuntu

docker run --name=httpd_temp rhel7:latest /bin/bash -c "yum install httpd -y;"

docker run -it --name ubuntu ubuntup

docker login -e

## イメージ一覧
docker images

## 起動してすぐログイン
docker run -it ccc6e87d482b bash
