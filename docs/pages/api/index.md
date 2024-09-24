## API usage

- Very experimental and some things may change in the future
- Only a few important endpoints are documented for now. If you need any more added, please join the Discord and let us know!

### Base URL

<code>http://{instance}/api</code>

- Replace `{instance}` with your instance domain or `ip:port`

### Endpoints

??? example "server-ping"
    #### Parameters

    | name      | type     | data type | description      |
    | --------- | -------- | --------- | ---------------- |
    | `request` | required | string    | endpoint name    |
    | `apikey`  | required | string    | instance api key |

    ##### Responses

    | http code | content-type       | response                                         |
    | --------- | ------------------ | ------------------------------------------------ |
    | `200`     | `application/json` | `{"code":"200","response":{"result":"v7.2.7"}}`  |
    | `423`     | `application/json` | `{"code":"423","error":"Migration in progress"}` |

    ##### Example cURL

    ```javascript
    curl -X GET -H "Content-Type: application/json" http://{instance}/api/?request=server-ping&apikey=<redacted>
    ```

??? example "stats-getContainersList"
    ##### Parameters

    | name      | type     | data type | description      |
    | --------- | -------- | --------- | ---------------- |
    | `request` | required | string    | endpoint name    |
    | `apikey`  | required | string    | instance api key |

    ##### Responses

    | http code | content-type       | response                                                                                          |
    | --------- | ------------------ | ------------------------------------------------------------------------------------------------- |
    | `200`     | `application/json` | [JSON](https://logs.notifiarr.com/?18b34487e18d801f#6ua883qJ6U6wPF6pAPyYCpZRp7P9cgwR75aGfPAtaz7c) |

    ##### Example cURL

    ```javascript
    curl -X GET -H "Content-Type: application/json" http://{instance}/api/?request=stats-getContainersList&apikey=<redacted>
    ```

??? example "stats-getOverview"
    ##### Parameters

    | name      | type     | data type | description      |
    | --------- | -------- | --------- | ---------------- |
    | `request` | required | string    | endpoint name    |
    | `apikey`  | required | string    | instance api key |

    ##### Responses

    | http code | content-type       | response                                                                                          |
    | --------- | ------------------ | ------------------------------------------------------------------------------------------------- |
    | `200`     | `application/json` | [JSON](https://logs.notifiarr.com/?c528e47b85d6beb4#CNGLgF5sbfWRUPuQ3UkPvWeRfJHP8dtJfn1HbZg4QoDH) |

    Usage values:

    - `disk` and `netIO` = bytes
    - `cpu` and `memory` = percentage

    ##### Example cURL

    ```javascript
    curl -X GET -H "Content-Type: application/json" http://{instance}/api/?request=stats-getOverview&apikey=<redacted>
    ```
