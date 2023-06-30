# Ssh setup
### Keys
1. Unix os (in client terminal)
 - Generate ssh key - 3x Enter
   ```bash
   ssh-keygen
   ```
- Push ssh key to server
   ```bash
   ssh-copy-id username@server_ip
   ```
### Protect
1. Change password
    ```bash
    sudo passwd user_name
    ```
2. protect your server access
   - AllowUsers **usernames**
   - PermitRootLogin no
   - PasswordAuthentication no
    ```bash
    sudo nano /etc/ssh/sshd_config
    ```
3. Restart ssh service
    ```bash
    sudo service ssh restart
    ```
