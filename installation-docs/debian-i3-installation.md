# Debian i3 Installation

The steps below work well with a Debian base installation as I covered in a [blog post](https://e33.io/913), and will install [i3](https://i3wm.org) with my [custom configurations and theming](https://github.com/e33io/dotfiles), along with a good base set of applications. The default configuration is for use with HiDPI monitors (192 dpi settings for 2x scaling), but there is an option at the end of the script that lets you change to standard HD monitors (96 dpi settings for 1x scaling). View my [custom keybindings](https://github.com/e33io/reference-wiki/tree/main/keybindings/i3-keybindings.md) to use session.

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

Step 4: Run the i3 script
```
sh debian-install-i3.sh
```

Step 5: At the end of the script you will see the option below for what type of monitor are you using, and answer `1` for Standard HD (96 dpi settings for 1x scaling), or `2` for HiDPI (192 dpi settings for 2x scaling)
```
=======================================================================
The option below lets you select a configuration specific
to your monitor type for proper display scaling.
=======================================================================
  1) Standard HD (96 dpi settings for 1x scaling)
  2) HiDPI (192 dpi settings for 2x scaling)
-----------------------------------------------------------------------
What type of monitor are you using?
```

Step 6: Reboot the PC
```
sudo reboot
```

&nbsp;
