## Docker

- Docker v25 or later
- Docker compose v2.27 or later

## Permissions

!!! info
    Dockwatch needs to be able to run docker based commands in order to function so this is important, alternative to Dockwatch using the docker.sock is if you use a [Socket proxy](/pages/misc/proxy)

Get the group id that docker uses with the following command

```
grep docker /etc/group
```

Get the user id from the user you want to run Dockwatch as with the following command:

```
id -u <username>
```
