# Arch Gnome Installation

The steps below work well with an [Arch](https://wiki.archlinux.org/title/Archinstall) "Minimal" (Profile > Type > Minimal) installation, and will install [Gnome](https://www.gnome.org) with my [custom configurations and theming](https://github.com/e33io/opt-dots), along with a good base set of applications. View my [custom keybindings](https://github.com/e33io/reference-wiki/tree/main/keybindings/gnome-keybindings.md) to use session.

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

Step 4: Run the Gnome script
```
sh arch-post-install-gnome.sh
```

Step 5: Reboot the PC
```
reboot
```

&nbsp;
