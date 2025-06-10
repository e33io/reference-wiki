# Fix Screen Tearing

### Configure X11 to fix screen tearing when not using a compositor

&nbsp;

## AMD

Create this file:
```
/etc/X11/xorg.conf.d/20-amdgpu.conf
```
Add and save:
```
Section "Device"
	Identifier "AMD Graphics"
	Driver     "amdgpu"
	Option     "TearFree" "true"
EndSection
```
NOTE: You will need `xserver-xorg-video-amdgpu` or `xf86-video-amdgpu` installed

&nbsp;

## Intel

Create this file:
```
/etc/X11/xorg.conf.d/20-intel.conf
```
Add and save:
```
Section "Device"
	Identifier "Intel Graphics"
	Driver     "intel"
	Option     "TearFree" "true"
EndSection
```
NOTE: You will need `xserver-xorg-video-intel` or `xf86-video-intel` installed

&nbsp;
