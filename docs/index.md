#### GitHub
![GitHub commit activity](https://img.shields.io/github/commit-activity/t/notifiarr/dockwatch?label=Commits&style=plastic)
![GitHub commit activity (branch)](https://img.shields.io/github/commit-activity/t/notifiarr/dockwatch/main?label=Main (:latest)&style=plastic)
![GitHub commit activity (branch)](https://img.shields.io/github/commit-activity/t/notifiarr/dockwatch/develop?label=Develop (:develop)&style=plastic)
![GitHub last commit (branch)](https://img.shields.io/github/last-commit/notifiarr/dockwatch/develop?label=Last (:develop)&style=plastic)
![GitHub contributors](https://img.shields.io/github/contributors/notifiarr/dockwatch?label=Contributors&style=plastic)

#### Support
[![Discord](https://img.shields.io/discord/764440599066574859?label=Discord&color=purple&style=plastic)](https://notifiarr.com/discord)

![Logo](assets/logo.png)

## Purpose

Simple UI driven way to manage updates & notifications for Docker containers. No external database is required, all settings are stored locally in an sqlite3 database.

## Project support

If the project is useful for you, do us a favor and smash that star button on the [Github](https://github.com/Notifiarr/dockwatch){:target="_blank"} page! If you want to support the project financially we do appreciate it and you can do that on the [Notifiarr Github](https://github.com/sponsors/Notifiarr){:target="_blank"} sponsor page. Added bonus with that is if you also use [Notifiarr](https://notifiarr.com){:target="_blank"} you can link your Github account and get patron perks there too!

## Features or bugs

If there is a feature you would like added or think you have found a bug, please join the discord and lets discuss it there in real time before doing a Github request. After we determine what to do (add a new feature or confirm the bug) we can move it to Github if necessary although most things can be fixed fast enough that it wont be needed.

## Notification options

### Triggers

- Container (re-)created/removed
- Container state changes (running -> stopped or healthy -> unhealthy)
- Update for container image tag is available
- Update for container image tag has been applied
- Orphan images, volumes & networks are pruned
- Memory and CPU usage is over a set limit

### Platforms

- Mattermost
- Notifiarr
- Telegram

## Updating options

Updates are applied on a container by container basis and use cron scheduling for flexibility

- Ignore updates
- Check for updates
- Auto update

## Other features

- Link and control multiple Dockwatch installs (other servers)
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

#### Servers

![Servers](assets/screenshots/interface/servers.png)

#### Overview

![Overview](assets/screenshots/interface/overview.png)

#### Containers

![Containers](assets/screenshots/interface/containers.png)

#### Container

![Container](assets/screenshots/interface/container.png)

#### Container compose

![ContainerCompose](assets/screenshots/interface/generate-compose.png)

#### Networks

![Networks](assets/screenshots/interface/networks.png)

#### Compose

![Compose](assets/screenshots/interface/compose.png)

#### Orphans

![Orphans](assets/screenshots/interface/orphans.png)

#### Notifications

![Notifications](assets/screenshots/interface/notifications.png)

#### Settings

![Settings](assets/screenshots/interface/settings.png)

#### Tasks

![Tasks](assets/screenshots/interface/tasks.png)

#### Commands

![Commands](assets/screenshots/interface/commands.png)

#### Logs

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
