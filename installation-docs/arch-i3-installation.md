# Arch i3 Installation

The steps below work well with an [Arch](https://wiki.archlinux.org/title/Archinstall) "Minimal" (Profile > Type > Minimal) installation, and will install [i3](https://i3wm.org) with my [custom configurations and theming](https://github.com/e33io/dots), along with a good base set of applications. The default configuration is for use with HiDPI monitors (192 dpi settings for 2x scaling), but there is an option at the end of the script that lets you change to standard HD monitors (96 dpi settings for 1x scaling). View my [custom keybindings](https://github.com/e33io/reference-wiki/tree/main/keybindings/i3-keybindings.md) to use session.

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

Step 4: Run the i3 script
```
sh arch-install-i3.sh
```

Step 5: Reboot the PC
```
reboot
```

&nbsp;
