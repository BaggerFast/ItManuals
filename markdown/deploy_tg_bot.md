# How to deploy python bot

This guide will be based on these templates:
- [TelegramBot](https://github.com/BaggerFast/AiogramTemplate)
- [DiscordBot](https://github.com/BaggerFast/NextcordTemplate)
 
All actions are suitable only for Os Linux and was tested on Ubuntu

## Bot setup
1. [Create virtual venv](venv.md)
2. ```pip install -r requirements.txt```


## Service setup
Services(Daemons) are programs that run on Linux in the background. They are usually loaded when the system boots.
1. Create Linux Service
    ```
    cd /etc/systemd/system
    sudo touch your-service-name.service
    ```
2. Edit Linux Service  
   ```
   sudo nano your-service-name.service
   ```
   [insert this template](../templates/bot.service)
   
   ```
   sudo systemctl daemon-reload
   ```

## How to use Service
1. Launch your service
   ```
   sudo systemctl start your-service-name.service
   ```
2. Enable service on reboot (autostart)
   ```
   sudo systemctl enable your-service-name.service
   ```
3. Disable service on reboot
   ```
   sudo systemctl disable your-service-name.service
   ```
4. Restart service - use after bot update
   ```
   sudo systemctl restart your-service-name.service
   ```
5. Get service status
   ```
   sudo systemctl status your-service-name.service
   ```
