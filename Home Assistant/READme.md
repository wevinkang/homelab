Have docker pre-installed, reference Docker/Docker Install.

Create directories and create docker-compose.yml file.
``` bash
sudo mkdir /opt/homeassistant
cd /opt/homeassistant
mkdir config

sudo nano /config/docker-compose.yml
```

Add the following to the file:
```
version: '3'
services:
  homeassistant:
    container_name: homeassistant
    image: "ghcr.io/home-assistant/home-assistant:stable"
    volumes:
      - /opt/homeassistant/config:/config
      - /etc/localtime:/etc/localtime:ro
    restart: unless-stopped
    privileged: true
    network_mode: host
```
Bring up container
``` bash
sudo docker compose up -d
```
