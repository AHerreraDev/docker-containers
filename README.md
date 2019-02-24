# Docker Node MongoDB Example

> Simple example of a dockerized Node/Mongo app

## Quick Start

```
# Run in Docker
docker-compose up
# use -d flag to run in background

# Tear down
docker-compose down

# To be able to edit files, add volume to compose file
volumes: ['./:/usr/src/app']

# To re-build
docker-compose build


# Install Docker-Compose in Linux VM
sudo curl -L https://github.com/docker/compose/releases/download/1.22.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

docker-compose --version

# Solve Docker daemon socket error:
sudo usermod -a -G docker $USER
Then, logout and log back in
```
