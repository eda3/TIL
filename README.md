# Docker

## system系のコマンド
### Dockerの実行環境確認
```
docker system info
```

### Dockerのディスク利用状況
```
docker system df
```

## container系のコマンド
### 起動中のコンテナプロセス一覧確認
```
docker container ps
```

### 特定のコンテナの詳細
```
docker container stats [NAMES]
```

### Ubuntuを入れてから起動するまで
```
docker pull ubuntu

docker run --name=httpd_temp rhel7:latest /bin/bash -c "yum install httpd -y;"

docker run -it --name ubuntu ubuntup

docker login -e

```

### イメージ一覧
```
docker images
docker image ls
```

### イメージの詳細確認
```
docker image inspect [イメージ]
```

### dockerイメージを起動してすぐログイン
```
docker run -it ccc6e87d482b bash
```

### 起動中のdockerプロセスにログイン
```
docker exec -it pedantic_morse bash
```

---

# Linux
```
apt-get update && apt-get upgrade

apt-get -y install build-essential curl git m4 ruby texinfo libbz2-dev libcurl4-openssl-dev libexpat-dev libncurses-dev zlib1g-dev

apt-get -y install build-essential curl file git
apt-get -y python3.8
apt install -y xclip
apt install -y ansible

```


## Gentoo Linux
### Change to root user
```
sudo su
```

### Make ssh key
```
sh-keygen -t rsa

useradd user -m -G users,wheel,tty -s /bin/bash
passwd user
```

### ssh
```

vi /etc/ssh/sshd_config
( Port 22 )
( Protocol 2 )

/etc/init.d/sshd start
```

### Docker
```
sudo emerge -av app-emulation/docker

groupadd docker

sudo usermod -a -G docker user

/etc/init.d/docker start

rc-update add docker default

systemctl start docker

systemctl enable docker
```

# PowerShell
## ワンライナー
### Windowsの環境変数PATHを改行区切りで表示させるワンライナー 

```
echo $env:path | % {$_ -replace(";","`r`n")}
```

# Vim
## 設定関連
### .vimrc読み込み先を一覧表示させる
```
:set runtimepath
```

# wasm
### rustupを入れる
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
export PATH="${PATH}:${HOME}/.cargo/bin"
```

### gnu版のrust toolchainをインストール/アンインストール
 ```
rustup toolchain install stable-x86_64-pc-windows-gnu
rustup toolchain uninstall stable-x86_64-pc-windows-gnu

 ```

### wasm-packをインストールする
```
curl https://rustwasm.github.io/wasm-pack/installer/init.sh -sSf | sh
```

# Git
### WindowsのGitのバージョンをあげる
```
git update-git-for-windows
```
