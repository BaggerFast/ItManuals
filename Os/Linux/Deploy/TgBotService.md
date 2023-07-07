# How to deploy python bot

This guide will be based on these templates:
- [TelegramBot](https://github.com/BaggerFast/AiogramTemplate)
- [DiscordBot](https://github.com/BaggerFast/NextcordTemplate)
 
All actions are suitable only for Os Linux and was tested on Debian, Ubuntu

## Project setup
1. ```cd path/to/project/directory```
2. [Create virtual venv](../../../Langs/Python/README.md)
3. ```pip install -r requirements.txt```


## Service setup
Services(Daemons) are programs that run on Linux in the background.  
They are usually loaded when the system boots.

1. Create Linux Service
    ```bash
    cd /etc/systemd/system
    sudo touch your-service-name.service
    ```
2. Edit Linux Service  
   [insert this template](Templates/Bot.service)
    ```bash
   sudo nano your-service-name.service
   ```
3. [Setup service (1-2)](../System/Systemd.md)