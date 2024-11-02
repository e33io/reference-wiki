# Hide Unmounted Drive Icons in File Managers

&nbsp;

Create this file:
```
/etc/udev/rules.d/10-local.rules
```

Find the drive(s) you want to hide, the examples below would be for `nvme1n1p3` and `sda2` drives

Add and save:
```
KERNEL=="nvme1n1p3",ENV{UDISKS_IGNORE}="1"
KERNEL=="sda2",ENV{UDISKS_IGNORE}="1"
```

Reboot system

&nbsp;
