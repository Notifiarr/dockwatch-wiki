!!! warning
    Make sure the socket proxy runs on the same network as Dockwatch

Dockwatch is compatible with a Socket proxy & tested with:

- LSIO
- Tecnativa

You need to enable the following (possibly more based on the version, future added permissions to the proxy, etc):

```
    - CONTAINERS=1
    - IMAGES=1
    - PORTS=1
    - NETWORKS=1
    - VOLUMES=1
```

You also need to make sure and use the `DOCKER_HOST` variable (--env or compose environment) with the example value `http://socket-proxy:2375` (this points to your socket-proxy container)
