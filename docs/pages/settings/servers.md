!!! warning
    Some features can not be controlled remotely as it can cause loops or issues in the main instance. Updating a remote instance, managing remote instance server settings, etc are some as an example. Almost everything is managemeable on remotes from the main instance.

If you install multiple Dockwatch instances on multiple servers, you can optionally control them all from the same interface.

- Server 1
- Server 2
- Server 3

When you install Dockwatch it sets an apikey for it by default and names the instance localhost. You can change the instance name for the multi-server drop down to whatever you want. 

Lets say `Server 1` is going to be the main instance here so you need to open Server 2 and go to its settings. Copy the apikey from Server 2 and in the Server 1 settings you will add the url to Server 2, the apikey and give it a name. Repeat this process for Server 3 and save the settings on Server 1.

Now when the page reloads you will have a drop down menu above the navigation with all the connected servers (Servers 1-3) to pick from. Whatever page you are on will reload with the remote server data if you swap between them.
