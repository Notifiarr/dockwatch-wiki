## Unraid

- Icons show up automatically using unraid labels

## Non Unraid

- It tries to match the container image to an icon from the [images repository](https://github.com/Notifiarr/images) (Feel free to add more icons to that repo for others to use)
- If the icon name is not the same as the official container image or the app has multiple container images then an alias would be used

### Internal alias

This can be modified to add more links to official images as needed and can be viewed [in the repository](https://github.com/Notifiarr/dockwatch/blob/main/root/app/www/public/container-alias.json )

### Custom alias

If you have your own custom container images that you want to point to an icon:

- Create `/config/container-alias.json` and use the same format as the internal file

Example:
```
{
  "pi-hole": ["pihole"],
  "https://www.pgadmin.org/static/COMPILED/assets/img/postgres-alt.svg": ["pgadmin4"]
  "/config/images/vaultwarden.png": ["vaultwarden/server"]
}
```

!!! info
    Dockwatch supports pointing to the images repository, an arbitrary URL or a local image

In the file there is a `"key":"value"` which determines where to find the image and which containers to apply them to

Key (where the image is):

- Notifiarr image repo file name (1st example)
- Full url (2nd example)
- Absolute local path relative to the container (3rd example)

Value (container/image)

- Container names (1st example)
- Image names (2nd example)
- Full image names (3rd example)
