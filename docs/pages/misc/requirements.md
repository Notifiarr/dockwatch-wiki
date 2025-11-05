## Docker

- Docker Version 25+
- Docker Compose Version 2.27+ (optional)

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
