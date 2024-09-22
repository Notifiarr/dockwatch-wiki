This modal will allow you to pick and choose which container updates when and its update settings

!!! info
    You have the option to set them in mass or container by container as well

## Update

Pick the update option you want

- `Ignore`: This will not check for updates or try to update the container at all
- `Check for updates`: This uses regctl to check for changes in the container and can alert you when an update is available but will not update the container
- `Auto update`: This will use regctl to check for a change and pull the changes as needed to automatically update the container and alert you when this happens

## Frequency

This is how often you want to do the update option (assuming you did not pick Ignore) and uses the standard cron frequency. There is a limitation to the minute selection to try and mitigate repositories being overloaded/abused for excessive update checking.

When you click on the frequency box you will get a popup to help pick the frequency you want for those who are not familiar with cron expression formats.

Here is how to understand cron frequency and Google provides a lot of infomration about this as well

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

## Mass changes

At the bottom is a drop down for picking the update option and a frequency selection box that can be used to apply to multiple/all containers at once.

### All

After you pick the drop down option you want and the frequency, click the `double up arrow` next to each one and it will apply that choice to all the containers

### Selective

After you pick the drop down option you want and the frequency, click the `single up arrow` next to each one and it will apply that choice to only the containers you have checked the box for
