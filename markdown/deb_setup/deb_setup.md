#  Debian/Ubuntu setup
1. Update packages
```    
sudo apt-get update & sudo apt-get upgrade
```
2. Install packages
```
sudo apt-get install -y tmux htop git curl wget unzip zip gcc build-essential make locales
```
3. Set time-zone
```
timedatectl set-timezone Europe/Moscow
```
4. Install languages
```
dpkg-reconfigure locales
```
5. [Ssh setup](ssh.md)