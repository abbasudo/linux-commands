# linux-commands

## user

### create 
```shell
adduser username
```
```shell
passwd username
```
```shell
deluser --remove-home username
```

### add to group 
```shell
getent group
```
```shell
usermod -a -G group1,group2 username
```
add user to all default groups:
```shell
usermod -a -G root,daemon,bin,sys,adm,tty,disk,lp,mail,news,uucp,man,proxy,kmem,dialout,fax,voice,cdrom,floppy,tape,sudo,audio,dip,www-data,backup,operator,list,irc,src,gnats,shadow,utmp,video,sasl,plugdev,staff,games,users,nogroup,systemd-journal,systemd-network,systemd-resolve,systemd-timesync,crontab,messagebus,input,kvm,render,syslog,tss,uuidd,tcpdump,ssh,landscape,admin,netdev,lxd,systemd-coredump username
```

## DNS
dns are in the following path:
```shell
/etc/resolv.conf
```
or in :
```shell
/etc/netplan
```
## docker

```shell
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```
```shell
 curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
```shell
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
```shell
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```
## docker-compose
```shell
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
```shell
sudo chmod +x /usr/local/bin/docker-compose
```
## php
```shell
sudo apt install software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt upgrade
sudo apt update
```
```shell
sudo apt install php8.0 php8.0-cli php8.0-common
```
```shell
apt install openssl php8.0-curl php8.0-json php8.0-mbstring php8.0-mysql php8.0-xml php8.0-zip php8.0-mysqlnd php8.0-opcache php8.0-pdo php8.0-calendar php8.0-ctype php8.0-exif php8.0-ffi php8.0-fileinfo php8.0-ftp php8.0-gd php8.0-gettext php8.0-iconv php8.0-mysqli php8.0-phar php8.0-posix php8.0-readline php8.0-shmop php8.0-sockets php8.0-sysvmsg php8.0-sysvsem php8.0-sysvshm php8.0-tokenizer
```
## composer
```shell
cd ~
curl -sS https://getcomposer.org/installer -o /tmp/composer-setup.php
```
```shell
sudo php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer
```
## sail
```shell
alias sail='[ -f sail ] && bash sail || bash vendor/bin/sail'
```
```shell
sail up -d
```
