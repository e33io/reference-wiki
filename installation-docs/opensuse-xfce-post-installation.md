# openSUSE Xfce (post-install) Package Installation and Custom Configuration

The steps below work well with an openSUSE Tumbleweed "Desktop with Xfce" installation as I covered in a [wiki document](https://github.com/e33io/reference-wiki/tree/main/installation-docs/opensuse-xfce-desktop-installation.md), and will install my [custom configurations and theming](https://github.com/e33io/opt-dots), along with a good base set of applications. The default configuration is for use with HiDPI monitors (Window Scaling 2x), but there is an option at the end of the script that lets you change to "Window Scaling 1x" settings for use with non-HiDPI monitors. View my [custom keybindings](https://github.com/e33io/reference-wiki/blob/main/keybindings/xfce-keybindings.md) to use session.

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

Step 4: Run the Xfce script, enter your password and answer yes (y) or trust always (a) to all prompts
```
sh opensuse-xfce-post-install.sh
```

Step 5: At the end of the script you will see the option below, and answer `n` (for no) to keep the default HiDPI settings or `y` (for yes) to change to non-HiDPI settings, then you will see “All done, you can now run other commands or reboot the PC” when the script is finished
```
NOTE: The configs that were installed with this script
are based on using HiDPI monitors (Window Scaling 2x).
The option below lets you change to "Window Scaling 1x"
settings for use with non-HiDPI monitors.
---------------------------------------------------------
Do you want to change to 'Window Scaling 1x' non-HiDPI settings? (y/n)
```

Step 6: Reboot the PC
```
sudo reboot
```

&nbsp;
