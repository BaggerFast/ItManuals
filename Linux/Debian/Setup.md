#  Debian/Ubuntu setup
1. Create sudo user
```
adduser your-username && usermod -aG sudo your-username
```
2. Update packages
```    
sudo apt-get update & sudo apt-get upgrade
```
3. Install packages
```
sudo apt-get install -y tmux htop exa nvim git curl wget unzip zip gcc build-essential make locales
```
4. Set time-zone
```
timedatectl set-timezone Europe/Moscow
```
5. Install languages
```
dpkg-reconfigure locales
```
6. Remove unused pakages
```
sudo apt-get autoremove
```
7. [Ssh setup](Ssh.md)