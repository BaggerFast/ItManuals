## How to use Service (Systemd, Daemons)

Use if new service file were added or updated
```
sudo systemctl daemon-reload
```

1. Start your service
   ```
   sudo systemctl start your-service-name.service
   ```
2. Enable autostart on reboot
   ```
   sudo systemctl enable your-service-name.service
   ```
3. Stop your service:
   ```
   sudo systemctl stop your-service-name.service
   ```
4. Disable autostart on reboot
   ```
   sudo systemctl disable your-service-name.service
   ```
5. Restart service - use after bot update
   ```
   sudo systemctl restart your-service-name.service
   ```
6. Get service status
   ```
   sudo systemctl status your-service-name.service
   ```
7. If service **status is not OK** (see log info):
   ```
   sudo journalctl -u your-service-name.service -b
   ```