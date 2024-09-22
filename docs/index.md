<center>
Github:<br>
![GitHub commit activity](https://img.shields.io/github/commit-activity/t/notifiarr/dockwatch?label=Commits&style=plastic)
![GitHub commit activity (branch)](https://img.shields.io/github/commit-activity/t/notifiarr/dockwatch/main?label=Main (:latest)&style=plastic)
![GitHub commit activity (branch)](https://img.shields.io/github/commit-activity/t/notifiarr/dockwatch/develop?label=Develop (:develop)&style=plastic)
![GitHub last commit (branch)](https://img.shields.io/github/last-commit/notifiarr/dockwatch/develop?label=Last (:develop)&style=plastic)
![GitHub contributors](https://img.shields.io/github/contributors/notifiarr/dockwatch?label=Contributors&style=plastic)

Support:<br>
[![Discord](https://img.shields.io/discord/764440599066574859?label=Discord&color=purple&style=plastic)](https://notifiarr.com/discord)

![Logo](assets/logo.png)
</center>

## Purpose

Simple UI driven way to manage updates & notifications for Docker containers. No external database is required, all settings are stored locally in an sqlite3 database.

## Notifications

### Triggers

- Container (re-)created/removed
- Container state changes (running -> stopped or healthy -> unhealthy)
- Update for container image tag is available
- Update for container image tag has been applied
- Orphan images, volumes & networks are pruned
- Memory and CPU usage is over a set limit

### Platforms

- Notifiarr
- Telegram

## Updating options

Updates are applied on a container by container basis and use cron scheduling for flexibility

- Ignore updates
- Check for updates
- Auto update

## Other features

- Link and control multiple dockwatch installs (other servers)
- Automatically locate and match container icons for non Unraid usage*
- Update schedules for container image tags by a container basis
- Notifications by a container basis
- Automatically try to restart unhealthy containers
- Mass prune orphan images, volumes & networks
- Mass actions for containers [(re-)start/stop, pull, update]**
- Group containers in a table view for easier management

\* If icon is available at [Notifiarr/images](https://github.com/Notifiarr/images)<br>
** Also includes generating a docker run command, docker-compose.yml and comparing mounts.

## Screenshots

!!! note

    These might differ slightly from time to time as the UI can change faster than the wiki might be updated.

### Interface

![Overview](assets/screenshots/interface/overview.png)
![Container](assets/screenshots/interface/containers.png)
![Orphans](assets/screenshots/interface/orphans.png)
![Notifications](assets/screenshots/interface/notifications.png)
![Settings](assets/screenshots/interface/settings.png)
![Tasks](assets/screenshots/interface/tasks.png)
![Commands](assets/screenshots/interface/commands.png)
![Logs](assets/screenshots/interface/logs.png)

### Notifiarr notifications

![Added](assets/screenshots/notifications/notifiarr/added.png)
![Prune](assets/screenshots/notifications/notifiarr/prune.png)
![StateChange](assets/screenshots/notifications/notifiarr/statechange.png)
![UpdatesApplied](assets/screenshots/notifications/notifiarr/updates-applied.png)
![UpdatesAvailable](assets/screenshots/notifications/notifiarr/updates-available.png)
![Usage](assets/screenshots/notifications/notifiarr/usage.png)

### Telegram notifications

![Added](assets/screenshots/notifications/telegram/added.png)
![CpuUsage](assets/screenshots/notifications/telegram/cpuusage.png)
![Health](assets/screenshots/notifications/telegram/health.png)
![MemUsage](assets/screenshots/notifications/telegram/memusage.png)
![Prune](assets/screenshots/notifications/telegram/prune.png)
![Removed](assets/screenshots/notifications/telegram/removed.png)
![StateChange](assets/screenshots/notifications/telegram/statechange.png)
![Updated](assets/screenshots/notifications/telegram/updated.png)
![Updates](assets/screenshots/notifications/telegram/updates.png)
