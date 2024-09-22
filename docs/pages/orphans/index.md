The orphans page will show you everything docker consideres orphaned and not in use

!!! info
    All orphans can be automatically cleaned up by using the [Auto Prune](/pages/settings/prune) setting

## Images

These are images that docker says should be able to be deleted safely. The command that fetches this list is also on the page so it can be run manually in your shell for verification

!!! example "Network command"
    ```
    docker images -f dangling=true
    ```

## Volumes

These are volumes that are no longer in use. Docker does not provide the actual paths where these volumes once pointed to so all that is available is the internal docker hash for the orphaned volume and the internal docker mount hash.

!!! example "Network command"
    ```
    docker volume ls -qf dangling=true
    ```

## Networks

These are past networks that where used and during updates have been new ids assigned to them so the old one is not in use anymore

!!! example "Network command"
    ```
    docker network ls -qf dangling=true
    ```
