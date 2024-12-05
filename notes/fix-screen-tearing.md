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
	Option     "TripleBuffer" "true"
	Option     "NoAccel" "True"
	Option     "DRI" "False"
EndSection
```

&nbsp;
