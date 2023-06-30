## How to use Service (Systemd, Daemons)

Use if new service file were added or updated
   ```bash
   sudo systemctl daemon-reload
   ```

1. Start your service
   ```bash
   sudo systemctl start your-service-name.service
   ```
2. Enable autostart on reboot
   ```bash
   sudo systemctl enable your-service-name.service
   ```
3. Stop your service:
   ```bash
   sudo systemctl stop your-service-name.service
   ```
4. Disable autostart on reboot
   ```bash
   sudo systemctl disable your-service-name.service
   ```
5. Restart service - use after bot update
   ```bash
   sudo systemctl restart your-service-name.service
   ```
6. Get service status
   ```bash
   sudo systemctl status your-service-name.service
   ```
7. If service **status is not OK** (see log info):
   ```bash
   sudo journalctl -u your-service-name.service -b
   ```