!!! warning
    Make sure the socket proxy runs on the same network as Dockwatch

Dockwatch is compatible with a Socket proxy & tested with:

- LSIO
- Tecnativa

You need to enable the following (possibly more based on the version, future added permissions to the proxy, etc):

```yaml
    - ALLOW_START=1
    - ALLOW_STOP=1
    - ALLOW_RESTARTS=1
    - CONTAINERS=1
    - IMAGES=1
    - PORTS=1
    - NETWORKS=1
    - POST=1
    - VOLUMES=1
```

You also need to make sure and use the `DOCKER_HOST` variable (--env or compose environment) with the example value `tcp://socket-proxy:2375` (this points to your socket-proxy container)
