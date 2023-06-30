# Docker setup
### Mac os / Windows
- https://www.docker.com/

### Debian based images 
1. Install docker
    ```bash
    curl -fsSl https://get.docker.com/ -o get-docker.sh && \
      sh get-docker.sh && \
      rm get-docker.sh
    ```
2. Install docker-compose
    ```bash
    apt install python3-pip && pip3 install docker-compose
    ```
3. Setup user roles
    ```bash
    sudo usermod -aG docker username
    ```
