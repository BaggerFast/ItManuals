## Mount usb drive on Linux
1) Mount only by GUID 
   - Label, Name, etc not static
   - GUID change after reformat
2) Create mount directory
   ```bash
   mkdir path/to/mount/point
   ```
3) View storages info (remember device name)
   ```bash
   sudo lsblk 
   ```
   Example 
   ```
   NAME                            MAJ:MIN RM   SIZE RO TYPE  MOUNTPOINT
   sda                               8:0    0   5.5T  0 disk  
   ├─sda1                            8:1    0   5.5T  0 part  
   └─sda9                            8:9    0     8M  0 part  
   sdb                               8:16   0   5.5T  0 disk  
   ├─sdb1                            8:17   0   5.5T  0 part  
   └─sdb9                            8:25   0     8M  0 part  
   ```
4) Get device GUID (take GUID by name)
   ```bash
   sudo blkid | grep "DeviceName"
   ```
   Example
   ```
   /dev/sdb2: UUID="41c22818-fbad-4da6-8196-c816df0b7aa8" SEC_TYPE="ext2" TYPE="ext3" 
   ```
5) Set auto mount after reboot
   ```bash
   nano /etc/fstab
   ```
   Paste last line with your options
   ```
   UUID={YOUR-GUID}    {/path/to/mount/point}               {file-system-type}    defaults,errors=remount-ro 0       1
   ```
6) Manual mount
   ```bash
   mount -a
   ```
7) Check MountPoint
   ```bash
   sudo lsblk
   ```
   ```
   NAME                            MAJ:MIN RM   SIZE RO TYPE  MOUNTPOINT
   sda                               8:0    0   5.5T  0 disk  
   ├─sda1                            8:1    0   5.5T  0 part  
   └─sda9                            8:9    0     8M  0 part  
   sdb                               8:16   0   5.5T  0 disk  
   ├─sdb1                            8:17   0   5.5T  0 part  
   └─sdb9                            8:25   0     8M  0 part  
   sdc                               8:32   0 298.1G  0 disk  
   └─sdc1                            8:33   0 298.1G  0 part  /mnt/backup
   ```

[Maybe helpful](https://www.cyberciti.biz/faq/linux-finding-using-uuids-to-update-fstab/)