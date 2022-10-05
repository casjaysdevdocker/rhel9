## 👋 Welcome to rhel9 🚀  

rhel9 README  
  
  
## Run container

```shell
dockermgr update rhel9
```

### via command line

```shell
docker pull casjaysdevdocker/rhel9:latest && \
docker run -d \
--restart always \
--name casjaysdevdocker-rhel9 \
--hostname casjaysdev-rhel9 \
-e TZ=${TIMEZONE:-America/New_York} \
-v $HOME/.local/share/srv/docker/rhel9/files/data:/data:z \
-v $HOME/.local/share/srv/docker/rhel9/files/config:/config:z \
-p 80:80 \
casjaysdevdocker/rhel9:latest
```

### via docker-compose

```yaml
version: "2"
services:
  rhel9:
    image: casjaysdevdocker/rhel9
    container_name: rhel9
    environment:
      - TZ=America/New_York
      - HOSTNAME=casjaysdev-rhel9
    volumes:
      - $HOME/.local/share/srv/docker/rhel9/files/data:/data:z
      - $HOME/.local/share/srv/docker/rhel9/files/config:/config:z
    ports:
      - 80:80
    restart: always
```

## Authors  

🤖 casjay: [Github](https://github.com/casjay) [Docker](https://hub.docker.com/r/casjay) 🤖  
⛵ CasjaysDevDocker: [Github](https://github.com/casjaysdevdocker) [Docker](https://hub.docker.com/r/casjaysdevdocker) ⛵  
