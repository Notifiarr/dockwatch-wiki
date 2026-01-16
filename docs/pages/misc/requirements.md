## Docker

- Docker Version 25+
- Docker Compose Version 2.27+ (optional)

!!! warning
    Starting with version [v0.6.472](https://github.com/Notifiarr/dockwatch/commit/3c5c037d2d75df261efdaf7a2b87e801ee3775e2), the internal Docker service has been updated to version 29. This means that if your host has a Docker service older than version 29 installed, you must add an extra [environment variable](/pages/misc/composeRun/#variables) to ensure that Dockwatch can connect to the host.

## Permissions

!!! info
    Dockwatch must be able to run Docker commands to function. This typically requires access to the Docker socket (docker.sock); alternatively, you can use a [socket proxy](/pages/misc/proxy).

Get the group id that Docker uses with the following command:

```
grep docker /etc/group
```

Get the user id from the user you want to run Dockwatch as with the following command:

```
id -u <username>
```
