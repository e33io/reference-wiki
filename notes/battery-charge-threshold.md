# Set Battery Charge Stop Threshold

### NOTE: I've only tested this on ThinkPad laptops

&nbsp;

Switch to root user:
```
sudo su
```

Run this command, edit the `90` value to whatever percentage you want to stop charging at:
```
echo 90 > /sys/class/power_supply/BAT0/charge_stop_threshold
```

Reboot system

&nbsp;
