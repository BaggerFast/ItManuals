# Ssh setup
### Keys
for login without password
1. Unix os (not in server terminal)
 - Generate ssh key - 3x Enter
```
ssh-keygen
```
- Push ssh key to server
```
ssh-copy-id username@server_ip
```
### Protect
1. Change password
```
sudo passwd user_name
```
2. protect your server access
```
sudo nano /etc/ssh/sshd_config
```
- AllowUsers **usernames**
- PermitRootLogin no
- PasswordAuthentication no
3. Restart ssh service
```
sudo service ssh restart
```
