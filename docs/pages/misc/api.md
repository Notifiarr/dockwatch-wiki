## Authorization

Header `X-Api-Key:{apikey}`<br>
Parameter `?apikey={apikey}`

!!! example
    ```
    curl -H "X-Api-Key:{apikey}" "http://{host}:9999/api/database/containers"
    ```

## Responses

All responses are JSON with possible response codes:

=== "200"
    Success
=== "400"
    Missing required param(s)
=== "401"
    Invalid apikey
=== "405"
    Invalid endpoint or method for the used endpoint

Success example:

``` json
{
    "code": 200,
    "response": {
        "result": ....
    }
}
```

Error example:

``` json
{
    "code": 405,
    "error": "Invalid GET request (endpoint=database/fake-endpoint)"
}
```

## /api/database/* - 25

### <span style="display:none;">container/add</span>

??? abstract "container/add"
    Endpoint: `/api/database/container/add`<br>
    Usage: Add a containers settings to the database
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `hash` | str | yes |
        | `updates` | int | no |
        | `frequency` | str | no |
        | `restartUnhealthy` | int | no |
        | `disableNotifications` | int | no |
        | `shutdownDelay` | int | no |
        | `shutdownDelaySeconds` | int | no |

### <span style="display:none;">container/group/add</span>

??? abstract "container/group/add"
    Endpoint: `/api/database/container/group/add`<br>
    Usage: Add a new container group to the database
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">container/group/delete</span>

??? abstract "container/group/delete"
    Endpoint: `/api/database/container/group/delete`<br>
    Usage: Remove a container group from the database
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `id` | int | yes |

### <span style="display:none;">container/hash</span>

??? abstract "container/hash"
    Endpoint: `/api/database/container/hash`<br>
    Usage: Get a container from the database using its hash
    === "GET"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `hash` | str | yes |

### <span style="display:none;">container/update</span>

??? abstract "container/update"
    Endpoint: `/api/database/container/update`<br>
    Usage: Get a container from the database using its hash
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `hash` | str | yes |
        | `updates` | int | no |
        | `frequency` | str | no |
        | `restartUnhealthy` | int | no |
        | `disableNotifications` | int | no |
        | `shutdownDelay` | int | no |
        | `shutdownDelaySeconds` | int | no |

### <span style="display:none;">containers</span>

??? abstract "containers"
    Endpoint: `/api/database/containers`<br>
    Usage: Return a list of containers that have settings in the database
    === "GET"
        No parameters

### <span style="display:none;">group/container/link/add</span>

??? abstract "group/container/link/add"
    Endpoint: `/api/database/group/container/link/add`<br>
    Usage: Add a container to a group
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `groupId` | int | yes |
        | `containerId` | int | yes |

### <span style="display:none;">group/container/link/remove</span>

??? abstract "group/container/link/remove"
    Endpoint: `/api/database/group/container/link/remove`<br>
    Usage: Remove a container from a group
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `groupId` | int | yes |
        | `containerId` | int | yes |

### <span style="display:none;">group/container/links</span>

??? abstract "group/container/links"
    Endpoint: `/api/database/group/container/links`<br>
    Usage: Return a list of containers linked to a group using its id
    === "GET"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `group` | int | yes |

### <span style="display:none;">group/container/update</span>

??? abstract "group/container/update"
    Endpoint: `/api/database/group/container/update`<br>
    Usage: Update the container group
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |
        | `id` | int | yes |

### <span style="display:none;">group/hash</span>

??? abstract "group/hash"
    Endpoint: `/api/database/group/hash`<br>
    Usage: Get a group from the database using its hash
    === "GET"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `hash` | str | yes |

### <span style="display:none;">group/links</span>

??? abstract "group/links"
    Endpoint: `/api/database/group/links`<br>
    Usage: Return a list of group/container links from the database
    === "GET"
        No parameters

### <span style="display:none;">groups</span>

??? abstract "groups"
    Endpoint: `/api/database/groups`<br>
    Usage: Return a list of groups from the database
    === "GET"
        No parameters

### <span style="display:none;">migrations</span>

??? abstract "migrations"
    Endpoint: `/api/database/migrations`<br>
    Usage: Trigger a migration check
    === "GET"
        No parameters

### <span style="display:none;">links</span>

??? abstract "links"
    Endpoint: `/api/database/links`<br>
    Usage: Return a list of notification/platform links
    === "GET"
        No parameters

### <span style="display:none;">notification/link/add</span>

??? abstract "notification/link/add"
    Endpoint: `/api/database/notification/link/add`<br>
    Usage: Add a new notification notifier to the database
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `platformId` | int | yes |
        | `triggerIds` | list | yes |
        | `platformParameters` | object | yes |
        | `senderName` | str | yes |

### <span style="display:none;">notification/link/delete</span>

??? abstract "notification/link/delete"
    Endpoint: `/api/database/notification/link/delete`<br>
    Usage: Remove a notification notifier from the database
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `linkId` | str | yes |

### <span style="display:none;">notification/link/platform/name</span>

??? abstract "notification/link/platform/name"
    Endpoint: `/api/database/notification/link/platform/name`<br>
    Usage: Get a notification link using its name
    === "GET"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">notification/link/update</span>

??? abstract "notification/link/update"
    Endpoint: `/api/database/notification/link/update`<br>
    Usage: Update an existing notification notifier in the database
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `linkId` | int | yes |
        | `platformId` | int | yes |
        | `triggerIds` | list | yes |
        | `platformParameters` | object | yes |
        | `senderName` | str | yes |

### <span style="display:none;">notification/platforms</span>

??? abstract "notification/platforms"
    Endpoint: `/api/database/notification/platforms`<br>
    Usage: Return a list of notification platforms
    === "GET"
        No parameters

### <span style="display:none;">notification/triggers</span>

??? abstract "notification/triggers"
    Endpoint: `/api/database/notification/triggers`<br>
    Usage: Return a list of notification triggers
    === "GET"
        No parameters

### <span style="display:none;">notification/trigger/enabled</span>

??? abstract "notification/trigger/enabled"
    Endpoint: `/api/database/notification/trigger/enabled`<br>
    Usage: Get enabled status for a specific notification using its id
    === "GET"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `trigger` | int | yes |

### <span style="display:none;">servers</span>

??? abstract "servers"
    Endpoint: `/api/database/servers`<br>
    Usage: Get/set a list of linked servers (other Dockwatch instances)
    === "GET"
        No parameters
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `serverList` | object | yes |

### <span style="display:none;">setting</span>

??? abstract "setting"
    Endpoint: `/api/database/setting`<br>
    Usage: U&pdate a setting
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `setting` | str | yes |
        | `value` | any | yes |

### <span style="display:none;">settings</span>

??? abstract "settings"
    Endpoint: `/api/database/settings`<br>
    Usage: Get/set a list of Dockwatch settings
    === "GET"
        No parameters
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `newSettings` | object | yes |

## /api/docker/* - 24

### <span style="display:none;">container/create</span>

??? abstract "container/create"
    Endpoint: `/api/docker/container/create`<br>
    Usage: Create a container from an inspect object
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `inspect` | object | yes |

### <span style="display:none;">container/inspect</span>

??? abstract "container/inspect"
    Endpoint: `/api/docker/container/inspect`<br>
    Usage: Return information about a container
    === "GET"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">container/kill</span>

??? abstract "container/kill"
    Endpoint: `/api/docker/container/kill`<br>
    Usage: Kill a container
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">container/logs</span>

??? abstract "container/logs"
    Endpoint: `/api/docker/container/logs`<br>
    Usage: Return the logs from a container
    === "GET"
        No parameters

### <span style="display:none;">container/pull</span>

??? abstract "container/pull"
    Endpoint: `/api/docker/container/pull`<br>
    Usage: Pull a container
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">container/ports</span>

??? abstract "container/ports"
    Endpoint: `/api/docker/container/ports`<br>
    Usage: Return a list of ports used by a container
    === "GET"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">container/remove</span>

??? abstract "container/remove"
    Endpoint: `/api/docker/container/remove`<br>
    Usage: Remove a container
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">container/restart</span>

??? abstract "container/restart"
    Endpoint: `/api/docker/container/restart`<br>
    Usage: Restart a container
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">container/start</span>

??? abstract "container/start"
    Endpoint: `/api/docker/container/start`<br>
    Usage: Start a container
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">container/stop</span>

??? abstract "container/stop"
    Endpoint: `/api/docker/container/stop`<br>
    Usage: Stop a container
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">create/compose</span>

??? abstract "create/compose"
    Endpoint: `/api/docker/create/compose`<br>
    Usage: Genertate a compose file for a container
    === "GET"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">create/run</span>

??? abstract "create/run"
    Endpoint: `/api/docker/create/run`<br>
    Usage: Genertate a docker run command for a container
    === "GET"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">image/remove</span>

??? abstract "image/remove"
    Endpoint: `/api/docker/image/remove`<br>
    Usage: Remove an image
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `image` | str | yes |

### <span style="display:none;">images/sizes</span>

??? abstract "images/sizes"
    Endpoint: `/api/docker/images/sizes`<br>
    Usage: Return a list of image sizes
    === "GET"
        No parameters

### <span style="display:none;">network/remove</span>

??? abstract "network/remove"
    Endpoint: `/api/docker/network/remove`<br>
    Usage: Remove a network
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">networks</span>

??? abstract "networks"
    Endpoint: `/api/docker/networks`<br>
    Usage: Return a list of the docker networks
    === "GET"
        No parameters

### <span style="display:none;">orphans/containers</span>

??? abstract "orphans/containers"
    Endpoint: `/api/docker/orphans/containers`<br>
    Usage: Return a list of containers
    === "GET"
        No parameters

### <span style="display:none;">orphans/networks</span>

??? abstract "orphans/networks"
    Endpoint: `/api/docker/orphans/networks`<br>
    Usage: Return a list of orphaned networks
    === "GET"
        No parameters

### <span style="display:none;">orphans/volumes</span>

??? abstract "orphans/volumes"
    Endpoint: `/api/docker/orphans/volumes`<br>
    Usage: Return a list of orphaned volumes
    === "GET"
        No parameters

### <span style="display:none;">permissions</span>

??? abstract "permissions"
    Endpoint: `/api/docker/permissions`<br>
    Usage: Check if the user:group has access to the docker sock
    === "GET"
        No parameters

### <span style="display:none;">processList</span>

??? abstract "processList"
    Endpoint: `/api/docker/processList`<br>
    Usage: Return the current docker processlist
    === "GET"
        No parameters

### <span style="display:none;">stats</span>

??? abstract "stats"
    Endpoint: `/api/docker/stats`<br>
    Usage: Returns the cached information used in the UI
    === "GET"
        No parameters

### <span style="display:none;">unused/containers</span>

??? abstract "unused/containers"
    Endpoint: `/api/docker/unused/containers`<br>
    Usage: Return a list of unused containers
    === "GET"
        No parameters

### <span style="display:none;">volume/remove</span>

??? abstract "volume/remove"
    Endpoint: `/api/docker/volume/remove`<br>
    Usage: Remove a volume
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `id` | str | yes |

## /api/dockerAPI/* - 1

### <span style="display:none;">container/create</span>

??? abstract "container/create"
    Endpoint: `/api/dockerAPI/container/create`<br>
    Usage: Recreate a container based on its inspect using the docker API
    === "GET"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

## /api/file/* - 5

### <span style="display:none;">dependency</span>

??? abstract "dependency"
    Endpoint: `/api/file/dependency`<br>
    Usage: Get/set the contents of the dependency json file
    === "GET"
        No parameters
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `contents` | json object | yes |

### <span style="display:none;">pull</span>

??? abstract "pull"
    Endpoint: `/api/file/pull`<br>
    Usage: Get/set the contents of the pull json file
    === "GET"
        No parameters
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `contents` | json object | yes |

### <span style="display:none;">sse</span>

??? abstract "sse"
    Endpoint: `/api/file/sse`<br>
    Usage: Get/set the contents of the sse json file
    === "GET"
        No parameters
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `contents` | json object | yes |

### <span style="display:none;">state</span>

??? abstract "state"
    Endpoint: `/api/file/state`<br>
    Usage: Get/set the contents of the state json file
    === "GET"
        No parameters
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `contents` | json object | yes |

### <span style="display:none;">stats</span>

??? abstract "stats"
    Endpoint: `/api/file/stats`<br>
    Usage: Get/set the contents of the stats json file
    === "GET"
        No parameters
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `contents` | json object | yes |

## /api/notification/* - 1

### <span style="display:none;">notification/test</span>

??? abstract "notification/test"
    Endpoint: `/api/notification/test`<br>
    Usage: Send a test notification to a specific trigger
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `linkId` | int | yes |
        | `name` | str | yes |

## /api/server/* - 5

### <span style="display:none;">log</span>

??? abstract "log"
    Endpoint: `/api/server/log`<br>
    Usage: Return a specific log contents
    === "GET"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `name` | str | yes |

### <span style="display:none;">log/delete</span>

??? abstract "log/delete"
    Endpoint: `/api/server/log/delete`<br>
    Usage: Delete a Specific log
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `log` | str | yes |

### <span style="display:none;">log/purge</span>

??? abstract "log/purge"
    Endpoint: `/api/server/log/purge`<br>
    Usage: Delete all logs in a group
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `group` | str | yes |

### <span style="display:none;">ping</span>

??? abstract "ping"
    Endpoint: `/api/server/ping`<br>
    Usage: Check if the instance is online
    === "GET"
        No parameters

### <span style="display:none;">task/run</span>

??? abstract "task/run"
    Endpoint: `/api/server/task/run`<br>
    Usage: Trigger a task to run
    === "POST"
        | Parameter | Type | Required |
        | ----- | ----- | ----- |
        | `task` | str | yes |

## /api/stats/* - 2

### <span style="display:none;">containers</span>

??? abstract "containers"
    Endpoint: `/api/stats/containers`<br>
    Usage: Returns the container list used by dashboard apps
    === "GET"
        No parameters

### <span style="display:none;">overview</span>

??? abstract "overview"
    Endpoint: `/api/stats/overview`<br>
    Usage: Returns the overview list used by dashboard apps
    === "GET"
        No parameters
