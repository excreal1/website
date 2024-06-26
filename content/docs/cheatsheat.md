+++
title = 'Cheatsheat'
date = 2024-06-03T04:11:59Z
draft = false
+++




```
#!/bin/bash

# Check if the script is being run as root
if [[ $EUID -ne 0 ]]; then
    echo "This script must be run as UMBWA!!" 
    exit 1
fi

# Add the current user to the docker group
sudo usermod -aG docker $USER

# Create a directory for Nginx Proxy Manager
mkdir /opt/nginx-proxy-manager

# Create a Docker Compose file
cat <<EOT >> /opt/nginx-proxy-manager/docker-compose.yml
version: '3'

services:
  app:
    image: jc21/nginx-proxy-manager:latest
    restart: unless-stopped
    ports:
      - '80:80'
      - '81:81'
      - '443:443'
    volumes:
      - ./data:/app/data
      - ./letsencrypt:/app/letsencrypt
    environment:
      DB_MYSQL_HOST: "db"
      DB_MYSQL_PORT: 3306
      DB_MYSQL_USER: "npm"
      DB_MYSQL_PASSWORD: "npm"
      DB_MYSQL_NAME: "npm"
    depends_on:
      - db

  db:
    image: jc21/mariadb-aria:latest
    restart: unless-stopped
    environment:
      MYSQL_ROOT_PASSWORD: 'npm'
      MYSQL_DATABASE: 'npm'
      MYSQL_USER: 'npm'
      MYSQL_PASSWORD: 'npm'
    volumes:
      - ./data/mysql:/var/lib/mysql
EOT

# Change permissions for the Docker Compose file
chmod 644 /opt/nginx-proxy-manager/docker-compose.yml

# Start Nginx Proxy Manager
cd /opt/nginx-proxy-manager
docker-compose up -d
```

