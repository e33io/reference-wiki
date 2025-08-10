# Debian Base Installation

This is a summary of the key settings and steps for a base install of [Debian](https://www.debian.org) with encryption, without a desktop environment. For detailed step-by-step instructions using the Debian Graphical Installer, please see my [blog post](https://e33.io/913), otherwise see the highlights below.

&nbsp;

## Partitions and software settings
- EFI Partition: 269 MiB, EFI System Partition, `/boot/efi`
- Boot Partition: 1024 MiB, Ext4, `/boot`
- Root Partition: use remaining space, Ext4, `/`
- Encrypt Root Partition: LUKS, mount to `/`
- Only select "standard system utilities" on Software selection screen (uncheck all the rest)

&nbsp;

## Set TTY font size for HiDPI monitors

Run this command:
```
sudo dpkg-reconfigure console-setup
```

Select `UFT-8` > `Latin1 and Latin5 - western Europe and Turkic languages` > `Terminus` > `16x32 (framebuffer only)`

Run `clear` command to clear the screen

&nbsp;

## Update APT sources list

Edit the `sources.list` file:
```
sudo nano /etc/apt/sources.list
```

Edit each listed source to include `main contrib non-free non-free-firmware`
```
deb http://deb.debian.org/debian trixie main contrib non-free non-free-firmware
deb-src http://deb.debian.org/debian trixie main contrib non-free non-free-firmware

deb http://deb.debian.org/debian-security/ trixie-security main contrib non-free non-free-firmware
deb-src http://deb.debian.org/debian-security/ trixie-security main contrib non-free non-free-firmware

deb http://deb.debian.org/debian trixie-updates main contrib non-free non-free-firmware
deb-src http://deb.debian.org/debian trixie-updates main contrib non-free non-free-firmware

#deb http://deb.debian.org/debian trixie-backports main contrib non-free non-free-firmware
#deb-src http://deb.debian.org/debian trixie-backports main contrib non-free non-free-firmware
```

Run this command:
```
sudo apt update && sudo apt upgrade
```

&nbsp;

## Install additional firmware

Run this command:
```
sudo apt install firmware-linux firmware-linux-nonfree
```

&nbsp;

## Make and setup a swap file

Run these commands:
```
sudo fallocate -l 2G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
```

Edit the `fstab` file:
```
sudo nano /etc/fstab
```

Add these lines:
```
# swap file
/swapfile swap swap defaults 0 0
```

Edit the `sysctl.conf` file:
```
sudo nano /etc/sysctl.conf
```

Add this line:
```
vm.swappiness=5
```

&nbsp;
