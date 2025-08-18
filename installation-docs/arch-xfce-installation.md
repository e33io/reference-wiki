# Arch Xfce Installation

The steps below work well with an [Arch](https://wiki.archlinux.org/title/Archinstall) "Minimal" (Profile > Type > Minimal) installation, and will install [Xfce](https://xfce.org) with my [custom configurations and theming](https://github.com/e33io/opt-dots), along with a good base set of applications. The default configuration is based on using 'Window Scaling 2x' for HiDPI monitors, but there is an option at the end of the script that lets you change to 'Window Scaling 1x' settings for use with standard HD monitors. View my [custom keybindings](https://github.com/e33io/reference-wiki/tree/main/keybindings/xfce-keybindings.md) to use session.

&nbsp;

Step 1: Install Git
```
sudo pacman -S git
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
sh arch-install-xfce.sh
```

Step 5: At the end of the script you will see the option below for what type of monitor are you using, and answer `1` for Standard HD (96 dpi settings for 'Window Scaling 1x'), or `2` for HiDPI (192 dpi settings for 'Window Scaling 2x')
```
################################################################
The option below lets you select a configuration specific
to your monitor type for proper display scaling.
################################################################
   1) Standard HD (96 dpi settings for 'Window Scaling 1x')
   2) HiDPI (192 dpi settings for 'Window Scaling 2x')
----------------------------------------------------------------
What type of monitor are you using?
```

Step 6: Reboot the PC
```
reboot
```

&nbsp;
