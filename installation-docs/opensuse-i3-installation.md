# openSUSE Tumbleweed i3 Installation

The steps below work well with an openSUSE Tumbleweed "Generic Desktop" base installation as I covered in a [wiki document](https://github.com/e33io/reference-wiki/tree/main/installation-docs/opensuse-generic-desktop-installation.md), and will install [i3](https://i3wm.org) with my [custom configurations and theming](https://github.com/e33io/dotfiles), along with a good base set of applications. The default configuration is for use with HiDPI monitors (192 dpi settings) and desktop-type computers, but there are options at the end of the script that let you change to 96 dpi settings for use with non-HiDPI monitors, and/or change to laptop-type (battery powered) computer settings. View my [custom keybindings](https://github.com/e33io/reference-wiki/tree/main/keybindings/i3-keybindings.md) to use session.

&nbsp;

Step 1: Install Git
```
sudo zypper install git
```

Step 2: Clone my [custom scripts](https://github.com/e33io/scripts)
```
git clone https://github.com/e33io/scripts
```

Step 3: Change the directory to the `scripts` directory
```
cd scripts
```

Step 4: Run the i3 script, enter your password and answer yes (y) or trust always (a) to all prompts
```
sh opensuse-post-install-i3.sh
```

Step 5: At the end of the script you will see the option below, and answer `n` (for no) to keep the default HiDPI settings or `y` (for yes) to change to non-HiDPI settings
```
NOTE: The configs that were installed with this script
are based on using HiDPI monitors (192 dpi settings).
The option below lets you change to 96 dpi settings for
use with non-HiDPI monitors.
---------------------------------------------------------
Do you want to change to 96 dpi non-HiDPI settings? (y/n)
```

Step 6: After the option above, you will see the option below, and answer `n` (for no) to keep the default desktop-type computer settings or `y` (for yes) to change to laptop-type computer settings, then you will see “All done, you can now run other commands or reboot the PC” when the script is finished
```
NOTE: The configs that were installed with this script
are based on using a desktop-type computer.
The option below lets you change to laptop configs for
use with a laptop-type (battery powered) computer.
---------------------------------------------------------
Do you want to change to laptop configs? (y/n)
```

Step 7: Reboot the PC
```
sudo reboot
```

&nbsp;
