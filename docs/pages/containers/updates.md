Use this modal to select which containers update, schedule when they update, and configure their update settings.

!!! info
    You can apply settings to multiple containers at once or configure each container individually.

## Update

Configure how updates are handled for each container:

- `Ignore` — do not check or apply updates for this container.
- `Check for updates` — check for available updates but do not apply them automatically.
- `Auto update` — apply updates automatically.
## Frequency

Configure how often the container update mechanism runs for each container.  
Dockwatch uses the power of cron for this. Below you can find an example on how cron works.  

```
* * * * * command to be executed
– – – – –
| | | | |
| | | | +—– day of week (0 – 6) (Sunday=0)
| | | +——- month (1 – 12)
| | +——— day of month (1 – 31)
| +———– hour (0 – 23)
+————- min (0 – 59)
```

## Minimum Age

You can set a minimum image age (the minimum time since an image was published) before an update becomes eligible to be applied.

## Mass changes

At the bottom, use the dropdown to choose an update action and the frequency selector to apply that choice to selected containers or to all containers at once.

### All

After selecting the desired action and frequency from the dropdown, click the `double up arrow` to apply the choice to all containers.

### Selective

After choosing the action and frequency, click the `single up arrow` beside each container to apply that choice only to the containers you have selected.
