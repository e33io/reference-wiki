# xdg-desktop-portal-gtk HiDPI scaling

&nbsp;

Run this command:
```
systemctl --user edit xdg-desktop-portal-gtk.service
```

Add this to the file in the designated section and save:
```
[Service]
Environment=GDK_SCALE=2
Environment=GDK_DPI_SCALE=0.5
```

Run these commands:
```
systemctl --user daemon-reload
systemctl --user restart xdg-desktop-portal-gtk
```

Reboot system

&nbsp;
