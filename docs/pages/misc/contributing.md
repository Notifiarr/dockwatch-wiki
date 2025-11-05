!!! info
    Tested on Debian 13.  
    If you're running Windows, please [open an issue](https://github.com/Notifiarr/dockwatch-wiki/issues/new) so we can add Windows-specific instructions.

- Fork the [repository](https://github.com/Notifiarr/dockwatch) and change directory with `cd dockwatch`
- Switch to `develop` branch with `git checkout develop`
- Run `sh docker/build.sh` ⇾ This will build a local image for Dockwatch
- You can now run this image with `docker compose -f docker/compose.yml up -d`

!!! warning
    If you're using a Linux distribution other than Ubuntu/Debian, update the `PUID` and `PGID` values in `docker/compose.yml` to match your user and group IDs. By default they are `PUID=1000` and `PGID=990`.
