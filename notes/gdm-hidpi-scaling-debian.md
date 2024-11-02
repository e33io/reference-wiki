# GDM HiDPI Scaling - Debian

&nbsp;

Edit this file:
```
/etc/gdm3/greeter.dconf-defaults
```

Add/edit the `scaling-factor` line and save:
```
[org/gnome/desktop/interface]
scaling-factor=uint32 2
```

Run this command:
```
sudo dpkg-reconfigure gdm3
```

Reboot system

&nbsp;
