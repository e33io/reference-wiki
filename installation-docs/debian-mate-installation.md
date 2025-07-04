# Debian MATE Installation

The steps below work well with a Debian base installation as I covered in a [blog post](https://e33.io/913), and will install [MATE](https://mate-desktop.org) with my [custom configurations and theming](https://github.com/e33io/opt-dots), along with a good base set of applications. View my [custom keybindings](https://github.com/e33io/reference-wiki/tree/main/keybindings/mate-keybindings.md) to use session.

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

Step 4: Run the MATE script
```
sh deb-post-install-mate.sh
```

Step 5: Reboot the PC
```
sudo reboot
```

&nbsp;
