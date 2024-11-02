# Debian LXQt Installation

The steps below work well with a Debian base installation as I covered in a [blog post](https://e33.io/913), and will install [LXQt](https://lxqt-project.org) with my [custom configurations and theming](https://git.sr.ht/~e33io/dotfiles), along with a good base set of applications. The default configuration is for use with HiDPI monitors (192 dpi settings), but there is an option at the end of the script that lets you change to 96 dpi settings for use with non-HiDPI monitors. View my [custom keybindings](https://git.sr.ht/~e33io/reference-wiki/tree/main/item/keybindings/lxqt-keybindings.md) to use session.

&nbsp;

Step 1: Install Git
```
sudo apt install git
```

Step 2: Clone my [custom scripts](https://git.sr.ht/~e33io/scripts)
```
git clone https://git.sr.ht/~e33io/scripts
```

Step 3: Change the directory to the `scripts` directory
```
cd scripts
```

Step 4: Run the LXQt script
```
sh deb-post-install-lxqt.sh
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

Step 6: Reboot the PC
```
systemctl reboot
```

&nbsp;
