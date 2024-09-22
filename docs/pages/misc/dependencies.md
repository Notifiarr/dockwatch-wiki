## Network dependencies

!!! info
    Dockwatch can automatically recognize if containers depend on specific network containers, for example Gluetun.

- Restart Gluetun -> restart dependencies
- Stop Gluetun -> stop dependencies
- Update Gluetun -> re-create dependencies with updated network mode attached
