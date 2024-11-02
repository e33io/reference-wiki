# LightDM GTK Greeter HiDPI Scaling

&nbsp;

Edit this file:
```
/etc/lightdm/lightdm.conf
```

Update this line in the `[Seat:*]` section and save:
```
[Seat:*]

greeter-wrapper=/etc/lightdm/Xgsession
```

Create a file:
```
/etc/lightdm/Xgsession
```

Add and save:
```
#!/bin/sh

# =========================================
# Wrapper to run around LightDM GTK Greeter
# =========================================

# Set HiDPI scaling
export GDK_SCALE=2

# Run greeter
exec $@
```

Run this command:
```
sudo chmod +x /etc/lightdm/Xgsession
```

Reboot system

&nbsp;
