# openSUSE Tumbleweed Generic Desktop Installation

[openSUSE Tumbleweed](https://www.opensuse.org/#Tumbleweed) is one of the most cutting edge Linux distributions, and installing it with encryption makes it extremely secure and private. The steps below detail the key steps of using the graphical installer to complete the base install with only a minimal "Generic Desktop" environment, using [Ext4](https://kernelnewbies.org/Ext4) instead of [Btrfs](https://btrfs.readthedocs.io/en/latest/Introduction.html) for the file system. This is a great base to install window managers like [i3](https://i3wm.org), etc.

&nbsp;

## Boot into the installer

Select > Yes, to activate online repositories

Use the default online repositories

Select > Generic Desktop

Select > Expert Partitioner > Start with Existing Partitions

Select the correct device and delete unneeded existing partitions

Select > Add Partition, and add the following partitions:
- 0.25 GiB > EFI Boot Partition > `/boot/efi`
- 1.0 GiB > Data and ISV Applications > Ext4 > `/boot`
- Remaining size > Data and ISV Applications > Ext4 > `/` > Encrypt Device, then enter passphrase
> NOTE: Make a [swap file](https://git.sr.ht/~e33io/reference-wiki/tree/main/item/installation-docs/opensuse-generic-desktop-installation.md#make-and-setup-a-swap-file) post-install instead of this stage

Select > Time Zone, then select your local time zone

Create New User, enter your new user credentials, and check/select "Use this password for system administrator", and uncheck/de-select "Automatic Login"

Select > Software (from the list)

Select > Details (at the bottom of Patterns list)

Uncheck/de-select the following from the Patterns tab:
- Select > X Window System
	- uncheck/de-select `patterns-base-x11_enhanced` (this helps keep the install more minimal)
	- uncheck/de-select `tigervnc` (Remmina is better if/when a VNC viewer is needed)
	- uncheck/de-select `xorg-x11-Xvnc`

Select > Search

Uncheck/de-select the following from the Search tab:
- Search `lightdm`
	- uncheck/de-select `lightdm-gtk-greeter` (this will auto-select lightdm-slick-greeter instead)

Check/select the following from Search tab:
- Search `plymouth`
	- check/select `plymouth`
- Search `sudo`
	- check/select `sudo`
- Search `git`
	- check/select `git`

Select > Accept > Continue

Select > Install

After the installer finishes, reboot system

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

## Set hostname

Run this command, but replace `new-host-name` with your new computer hostname
```
sudo hostnamectl set-hostname new-host-name
```

&nbsp;

## Add user to wheel group
Reference: https://en.opensuse.org/SDB:Administer_with_sudo

Run this command
```
sudo EDITOR=nano /usr/sbin/visudo
```

Uncomment this line
```
%wheel        ALL=(ALL)       ALL
```

Save and exit

Run this command, but replace `username` with your actual username
```
sudo /usr/sbin/usermod -aG wheel username
```

Run this command
```
sudo EDITOR=nano /usr/sbin/visudo
```

Comment out these lines
```
#Defaults targetpw    # ask for the password of the target user i.e. root
#ALL ALL=(ALL) ALL # WARNING! Only use this together with 'Defaults targetpw'!
```

Save and exit, then reboot system

&nbsp;

## Update system

Run this command, use the `--no-recommends` flag when updating the system to only install required packages
```
sudo zypper dup --no-recommends
```

&nbsp;

## Install codecs to enable VA-API hardware video acceleration

Run this command, answer yes (y), trust always (a) or solution (1) to all prompts, then reboot the system
```
sudo opi codecs
```

&nbsp;
