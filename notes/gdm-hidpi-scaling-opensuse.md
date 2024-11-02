# GDM HiDPI Scaling - openSUSE

&nbsp;

Create a file:
```
/etc/dconf/db/gdm.d/10-hidpi-gdm-settings
```

Add and save:
```
[org/gnome/desktop/interface]
scaling-factor=uint32 2
```

Create (or edit) this file:
```
/etc/dconf/profile/gdm
```

Add and save:
```
user-db:user
system-db:gdm
file-db:/usr/share/gdm/greeter-dconf-defaults
```

Run this command:
```
sudo dconf update
```

Reboot system

&nbsp;
