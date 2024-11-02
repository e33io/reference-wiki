# Debian Cinnamon Installation

The steps below work well with a Debian base installation as I covered in a [blog post](https://e33.io/913), and will install [Cinnamon](https://projects.linuxmint.com/cinnamon) with my [custom configurations and theming](https://git.sr.ht/~e33io/dotfiles), along with a good base set of applications. View my [custom keybindings](https://git.sr.ht/~e33io/reference-wiki/tree/main/item/keybindings/cinnamon-keybindings.md) to use session.

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

Step 4: Run the Cinnamon script
```
sh deb-post-install-cinnamon.sh
```

Step 5: Reboot the PC
```
systemctl reboot
```

&nbsp;
