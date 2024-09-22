!!! info
    Make sure you change the volumes, ports, etc to match your system

## Environment variables

### Volumes

| Name | Host | Container |
| ----- | ----- | ----- |
| App config | /mnt/disk1/appdata/dockwatch/config | /config |
| Docker sock | /var/run/docker.sock | /var/run/docker.sock |

### Ports

| Inside | Outside |
| ----- | ----- |
| 80 | 9999 |

### Variables

| Name | Key | Value |
| ----- | ----- | ----- |
| DOCKER_HOST (optional: only for socket proxy) | DOCKER_HOST | ip:port |
| PUID | PUID | 1001 |
| PGID | PGID | 999 |
| TZ | TZ | America/New_York |

## Run

```
docker run \
  -d \
  --name "/dockwatch" \
  --volume "/home/dockwatch/config:/config:rw" \
  --volume "/var/run/docker.sock:/var/run/docker.sock:rw" \
  --restart "unless-stopped" \
  --publish "9999:80/tcp" \
  --network "bridge" \
  --env "TZ=America/New_York" \
  --env "PUID=1001" \
  --env "PGID=999" \
  "ghcr.io/notifiarr/dockwatch:main"
```

## Compose

```
services:
  dockwatch:
    container_name: dockwatch
    image: ghcr.io/notifiarr/dockwatch:main
    restart: unless-stopped
    ports:
      - 9999:80/tcp
    environment:
      #-DOCKER_HOST=127.0.0.1:2375 # Uncomment and adjust accordingly if you use a socket proxy
      - PUID=1001
      - PGID=999
      - TZ=America/New_York
    volumes:
      - /home/dockwatch/config:/config
      - /var/run/docker.sock:/var/run/docker.sock # Comment this line if you use a socket proxy
```

## Repository

`ghcr.io/notifiarr/dockwatch:main` Safest option, recommended branch to use<br>
`ghcr.io/notifiarr/dockwatch:develop` Typically safe<br>
`ghcr.io/notifiarr/dockwatch:nightly` Typically only used for large major changes that need testing prior to develop<br>
