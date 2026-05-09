# Artix i3 Installation

The steps below work well with an [Artix](https://artixlinux.org) "base" installation, and will install [i3](https://i3wm.org) with my [custom configurations and theming](https://github.com/e33io/dots), along with a good base set of applications. View my [custom keybindings](https://github.com/e33io/reference-wiki/tree/main/keybindings/i3-keybindings.md) to use session.

&nbsp;

Step 1: Install Git
```
sudo pacman -S git
```

Step 2: Clone my [artix-i3](https://github.com/e33io/artix-i3) repo
```
git clone https://github.com/e33io/artix-i3
```

Step 3: Change the directory to the `artix-i3` directory
```
cd artix-i3
```

Step 4: Run the i3 script
```
sh install.sh
```

Step 5: Reboot the PC
```
sudo reboot
```

&nbsp;
