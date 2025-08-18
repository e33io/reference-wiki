# Debian Gnome Installation

The steps below work well with a Debian base installation as I covered in a [blog post](https://e33.io/913), and will install [Gnome](https://www.gnome.org) with my [custom configurations and theming](https://github.com/e33io/opt-dots), along with a good base set of applications. View my [custom keybindings](https://github.com/e33io/reference-wiki/tree/main/keybindings/gnome-keybindings.md) to use session. NOTE: See [optional steps](https://github.com/e33io/reference-wiki/tree/main/installation-docs/debian-gnome-installation.md#optional-disable-2x-scaling-on-plymouth-screen-and-gdm-display-manager) 6 and 7 to set 2x scaling on Plymouth screen and GDM display manager, for use with HiDPI monitors.

&nbsp;

Step 1: Install Git
```
sudo apt install git
```

Step 2: Clone my [custom scripts](https://github.com/e33io/scripts)
```
git clone https://github.com/e33io/scripts
```

Step 3: Change the directory to the `scripts` directory
```
cd scripts
```

Step 4: Run the Gnome script
```
sh debian-install-gnome.sh
```

Step 5: Reboot the PC
```
sudo reboot
```

&nbsp;

## Option: Set 2x scaling on Plymouth screen and GDM display manager

Step 6: Edit the `greeter.dconf-defaults` file
```
sudo nano /etc/gdm3/greeter.dconf-defaults
```

Un-comment the following line
```
scaling-factor=uint32 2
```

Step 7: Edit the `plymouthd.conf` file
```
sudo nano /etc/plymouth/plymouthd.conf
```

Un-comment the following line
```
DeviceScale=2
```

&nbsp;
