The containers table is straightforward.

## Column visibility

Select which columns to display — toggle any column on or off to customize the table view.

## Search

Search containers by name — enter a full or partial name to filter the table.

## Real time updates (SSE)

Auto refresh the table rows every 60 seconds, if the SSE task is enabled.

### Columns

If you utilize groups, they are listed first in the table and you click on the group name to show the container information for the group

`Name`: Click on a container to get a menu, from that menu you can make container specific changes and see some information about the container such as its network, labels, environment variables, etc. Under the container name is the repository for that container. *NOTE* Editing containers will show the interface but does not have a save button yet as it is still a WIP

`Updates`: This shows you information about your container setting with updates on or off. If updates are on (check only or apply) it will show you either "Outdated" or "Up to date" for the container. If you have it set to ignore it will show you "Ignored". Under the status is the current hash for the image you have.

`State`: This is the current state of the container (running, exited, created, etc) and the amount of time the container has been in that state

`Health`: This column will show you the health status of the container if it supports it and an icon to show if you have auto restart unhealthy on or off

`Mounts`: This column shows you all the mounts the given container has, the initial view is truncated but you can click the [+] icon to view them all

`Environment`: This column shows you all the environment variables the given container has, the initial view is truncated but you can click the [+] icon to view them all

`Ports`: This column shows you all the ports the given container uses, the initial view is truncated but you can click the [+] icon to view them all

`CPU/MEM`: This column shows your container usage per dockers usage (not entire server)
