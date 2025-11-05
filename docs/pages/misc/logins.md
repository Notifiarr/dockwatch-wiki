!!! warning
    It is strongly recommended to use a [reverse proxy](/pages/misc/composeRun/#reverse-proxy) with authentication instead.

Dockwatch has basic functionality for protecting the UI with a username and password.

- Create file logins in /config (should be `/config/logins`)
- Add `admin:password` to the file and save it (change this to your login)
- For multiple logins, drop a line and add another `admin:password`

There are [settings](/pages/settings/logins) to limit the amount of login failures and the timeout length for failed logins.
