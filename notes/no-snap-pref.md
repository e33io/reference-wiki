# Remove and Disable Snaps - Debian and Ubuntu

&nbsp;

### Stop and disable Snap service (if installed)

Run these commands:
```
sudo systemctl stop snapd.service
sudo systemctl disable snapd.service
```

&nbsp;

### Find and remove Snaps (if installed)

Find installed snaps: `snap list`

Remove installed snaps: `sudo snap remove <package>`

Remove snapd: `sudo apt purge snapd`

Remove snap directory from home: `rm -rf ~/snap`

Remove snap cache: `sudo rm -rf /var/cache/snapd`

&nbsp;

### Disable Snaps from being installed

Create this file:
```
/etc/apt/preferences.d/nosnap.pref
```
Add and save:
```
Package: snapd
Pin: release a=*
Pin-Priority: -10
```

Reboot system

&nbsp;
