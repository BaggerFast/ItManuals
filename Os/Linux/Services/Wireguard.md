# WireGuard Vpn Setup

#### [Download app](https://www.wireguard.com/install/)

1. Buy VPS Server, **which has ip in other country**
2. Connect via **ssh**
3. [Configure linux](../Debian/README.md)
4. Install packages (Ubuntu/Debian)
    ```bash
    sudo apt-get install curl
    ```
5. Setup wireguard via PiVpn
    ```bash
    curl -L https://install.pivpn.io | bash
    ```
6. Add new user
    ```bash
    pivpn add    
    ```
7. Help
    ```bash
    pivpn --help
    ```
**Important: 1 device = 1 config**