# WireGuard Vpn Setup

#### [Download app](https://www.wireguard.com/install/)

1. Buy VPS Server, which has ip in other country
2. Connect via Ssh
3. Install packages (Ubuntu/Debian)
```
sudo apt-get install curl
```
4. Setup wireguard via PiVpn
```
curl -L https://install.pivpn.io | bash
```
5. Add new user
```
pivpn add
```
6. Help
```
pivpn --help
```

**Important: 1 device = 1 config**
