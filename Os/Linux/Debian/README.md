#  Debian/Ubuntu setup
1. Create sudo user
    ```bash
    adduser your-username && usermod -aG sudo your-username
    ```
2. Update packages
    ```bash
    sudo apt-get update & sudo apt-get upgrade
    ```
3. Install packages
    ```bash
    sudo apt-get install -y btop tmux exa nvim git curl wget make unzip zip gcc build-essential make locales
    ```
4. Set time-zone
    ```bash
    timedatectl set-timezone Europe/Moscow
    ```
5. Install languages
    ```bash
    dpkg-reconfigure locales
    ```
6. Remove unused packages
    ```bash
    sudo apt-get autoremove
    ```
7. [Docker setup](../../../Tech/Docker/README.md)
8. [Ssh setup](Ssh.md)
