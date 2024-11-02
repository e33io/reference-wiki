# Root User Theming 

&nbsp;

### Link user theming to root user

Run these commands:
```
sudo mkdir -p /root/.config/gtk-3.0
sudo mkdir -p /root/.config/qt5ct
sudo ln -s $HOME/.config/gtk-3.0/settings.ini /root/.config/gtk-3.0/settings.ini
sudo ln -s $HOME/.config/qt5ct/qt5ct.conf /root/.config/qt5ct/qt5ct.conf
sudo ln -s $HOME/.gtkrc-2.0 /root/.gtkrc-2.0
```

&nbsp;
