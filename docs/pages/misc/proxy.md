!!! warning
    Make sure the socket proxy runs on the same network as Dockwatch.

Dockwatch is compatible with a Socket proxy & tested with:

- LSIO
- Tecnativa

Enable at least the following proxy permissions (additional permissions may be required depending on the proxy version or future updates):

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

You also need to make sure and use the [`DOCKER_HOST` variable](/pages/misc/composeRun/#variables).
