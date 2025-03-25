# Debian Xfce Installation

The steps below work well with a Debian base installation as I covered in a [blog post](https://e33.io/913), and will install [Xfce](https://xfce.org) with my [custom configurations and theming](https://github.com/e33io/opt-dots), along with a good base set of applications. The default configuration is based on using 'Window Scaling 2x' for HiDPI monitors, but there is an option at the end of the script that lets you change to 'Window Scaling 1x' settings for use with non-HiDPI monitors. View my [custom keybindings](https://github.com/e33io/reference-wiki/tree/main/keybindings/xfce-keybindings.md) to use session.

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

Step 4: Run the Xfce script
```
sh deb-post-install-xfce.sh
```

Step 5: At the end of the script you will see the option below, and answer `n` (for no) to keep the default HiDPI settings or `y` (for yes) to change to non-HiDPI settings, then you will see “All done, you can now run other commands or reboot the PC” when the script is finished
```
NOTE: The configs that were installed with this script
are based on using 'Window Scaling 2x' for HiDPI monitors.
The option below lets you change to 'Window Scaling 1x'
settings for use with non-HiDPI monitors.
----------------------------------------------------------------
Do you want to change to 'Window Scaling 1x' non-HiDPI settings?
```

Step 6: Reboot the PC
```
systemctl reboot
```

&nbsp;
