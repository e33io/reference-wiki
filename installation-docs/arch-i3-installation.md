# Arch i3 Installation

The steps below work well with an [Arch](https://wiki.archlinux.org/title/Archinstall) "Minimal" (Profile > Type > Minimal) installation, and will install [i3](https://i3wm.org) with my [custom configurations and theming](https://github.com/e33io/dots), along with a good base set of applications. View my [custom keybindings](https://github.com/e33io/reference-wiki/tree/main/keybindings/i3-keybindings.md) to use session.

&nbsp;

Step 1: Install Git
```
sudo pacman -S git
```

Step 2: Clone my [arch-i3](https://github.com/e33io/arch-i3) repo
```
git clone https://github.com/e33io/arch-i3
```

Step 3: Change the directory to the `arch-i3` directory
```
cd arch-i3
```

Step 4: Run the i3 script
```
sh install.sh
```

Step 5: Reboot the PC
```
reboot
```

&nbsp;
