## Option 1

- Fork the repo
- Create a directory symlink of the forked repo to /config/www.
  - Linux example: ln -s /home/user/dockwatch-git /home/user/config/www
  - Windows example: mklink /D "C:\dockwatch-git" "C:\dockwatch-config\www"
- Open the UI, Navigate to Settings->Development and set environment from Internal to External
- Save and restart Dockwatch container

## Option 2

- Fork the repo
- Open the Dockerfile and comment out the COPY root/ / line at the bottom
- Copy the files from root/app/www/public/\* to /config/www/\*
- Copy the cron from root/etc/crontabs/abc to /config/crontabs/abc (You'll need to add an ENV variable for DOCKER_MODS=linuxserver/mods:universal-cron)
- Copy the ini from root/etc/php82/conf.d/dockwatch.ini to /config/php/php-local.ini
- This should allow you to run the container while making changes to the files in /config and when done, just copy the files back into the root/ directories and push your fork so it builds a new container
