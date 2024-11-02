# Replace default Gnome Files app with Nemo - Debian

&nbsp;

Install nemo and nemo-fileroller:
```
sudo apt install nemo nemo-fileroller
```

Run these commands:
```
xdg-mime default nemo.desktop inode/directory application/x-gnome-saved-search
mkdir -p ~/.local/share/dbus-1/services
ln -s /usr/share/dbus-1/services/nemo.FileManager1.service ~/.local/share/dbus-1/services/
```

Reboot system

&nbsp;
