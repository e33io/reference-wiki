# Virt-Manager Setup - Debian and Ubuntu

&nbsp;

Install virt-manager
```
sudo apt install virt-manager
```

Edit this file:
```
/etc/libvirt/libvirtd.conf
```

Find and edit/uncomment the lines below, and save the file:
```
unix_sock_group = 'libvirt'

unix_sock_rw_perms = '0770'
```

Edit this file:
```
/etc/libvirt/qemu.conf
```

Find and edit/uncomment the lines below, replace `username` with your actual username, and save the file:
```
# Some examples of valid values are:
#
#       user = "qemu"   # A user named "qemu"
#       user = "+0"     # Super user (uid=0)
#       user = "100"    # A user named "100" or a user with uid=100
#
user = "username"

# The group for QEMU processes run by the system instance. It can be
# specified in a similar way to user.
group = "libvirt"
```

Run the commands below:
```
sudo usermod -a -G libvirt $(whoami)
sudo virsh net-autostart default
```

To check status, run the commands below:
```
sudo systemctl status libvirtd
sudo virsh net-list --all
```

&nbsp;
