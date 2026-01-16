!!! info
    Adjust the volumes, port mappings, and environment variables (including PUID/PGID and TZ) to match the paths, ports, and user/group IDs on your host system.

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

!!! info
    `DOCKER_HOST` only needs to be set when connecting via a [socket proxy](/pages/misc/proxy).

!!! info
    You can find the minimum API version value for `DOCKER_API_VERSION` by running `/usr/bin/docker version | grep -oP '(?<=minimum version )[\d.]+'` on your host. This is only needed if you have a Docker service installed that is older than version 29.


| Name | Key | Value |
| ----- | ----- | ----- |
| DOCKER_HOST | DOCKER_HOST | ip:port |
| DOCKER_API_VERSION | DOCKER_API_VERSION | 1.44 |
| PUID | PUID | 1001 |
| PGID | PGID | 999 |
| TZ | TZ | America/New_York |

## Docker Run

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

## Docker Compose

```
services:
  dockwatch:
    container_name: dockwatch
    image: ghcr.io/notifiarr/dockwatch:main
    restart: unless-stopped
    ports:
      - 9999:80/tcp
    environment:
      # - DOCKER_HOST=127.0.0.1:2375 # Uncomment and adjust accordingly if you use a socket proxy
      - PUID=1001
      - PGID=999
      - TZ=America/New_York
    volumes:
      - /home/dockwatch/config:/config
      - /var/run/docker.sock:/var/run/docker.sock # Comment this line if you use a socket proxy
```

## Repository

| Repository | Use-case |
| ----- | ----- |
| ghcr.io/notifiarr/dockwatch:main | Recommended branch to use |
| ghcr.io/notifiarr/dockwatch:develop | Typically safe — may include occasional bugs or unfinished changes |
| ghcr.io/notifiarr/dockwatch:nightly | Only used for major changes that require further testing |

## Reverse Proxy

Dockwatch can run behind a reverse proxy (for example, [sample Nginx config](https://github.com/Notifiarr/dockwatch/blob/develop/docker/nginx.conf)).  
Set Dockwatch Base URL in the Web UI settings to the path used by the proxy (for example `/dockwatch`). 

!!! warning
    If you cannot access the Web UI, create a file named `base-url.txt` in the app config directory containing the desired path (for example `/dockwatch`). Restart the container after changing the Base URL (via the UI or the file) to apply the setting.
