# sddm-hyprenv-theme :
![image](https://github.com/user-attachments/assets/d952c52e-bf3f-46a5-90b7-5273aec67506)
It's written using the latest version of Qt, which is **Qt6**. Its key features include **virtual keyboard support**. This theme also support **animated wallpapers**. You can easily change its appearance by choosing another of the 5 pre-made themes or creating your own.

> [!NOTE]
> All themes were created for 1080p. However, they should work well in other resolutions.


## Installation :

### Manual Installation

1. Install **dependencies**

[`sddm >= 0.21.0`](https://github.com/sddm/sddm), [`qt6 >= 6.8`](https://doc.qt.io/qt-6/index.html), [`qt6-svg >= 6.8`](https://doc.qt.io/qt-6/qtsvg-index.html), [`qt6-virtualkeyboard >= 6.8`](https://doc.qt.io/qt-6/qtvirtualkeyboard-index.html), [`qt6-multimedia >= 6.8`](https://doc.qt.io/qt-6/qtmultimedia-index.html)

You may also want to install additional video codecs like h.264.

```sh
sddm qt6-svg qt6-virtualkeyboard qt6-multimedia-ffmpeg     # Arch
sddm qt6-svg qt6-virtualkeyboard qt6-multimedia            # Void
sddm qt6-qtsvg qt6-qtvirtualkeyboard qt6-qtmultimedia      # Fedora
sddm-qt6 libQt6Svg6 qt6-virtualkeyboard qt6-virtualkeyboard-imports qt6-multimedia qt6-multimedia-imports        # OpenSUSE
sddm libqt6svg6 qt6-virtualkeyboard-plugin libqt6multimedia6 qml6-module-qtquick-controls qml6-module-qtquick-effects # Debian Unstable
```

2. Clone this repository
```
git clone https://github.com/Ayu-0/sddm-hyprenv-theme.git
```
3. Copy theme to `/usr/share/sddm/themes/`
```
sudo cp -r sddm-hyprenv-theme /usr/share/sddm/themes
```
4. Copy fonts to `/usr/share/fonts/`
```
sudo cp -r /usr/share/sddm/themes/sddm-hyprenv-theme/Fonts/* /usr/share/fonts/
```
5. Create a file theme.conf inside /etc/sddm.conf.d, If directory not exits then create it by running
```
sudo mkdir -p /etc/sddm.conf.d
```
```
sudo nano /etc/sddm.conf.d/theme.conf
```
6. And following contents to theme.conf
```
[Theme]
Current=sddm-hyprenv-theme
```
8. Edit `/etc/sddm.conf.d/virtualkbd.conf`
```sh
[General]
InputMethod=qtvirtualkeyboard" | sudo tee /etc/sddm.conf.d/virtualkbd.conf
```

## Selecting a theme

* By default `purple-heart` theme is active, there is conf file named theme.conf in sddm-hyprenv-theme folder.
* So, If you want to change theme, you have to select your theme from /Themes dir & rename it theme.conf and paste it into /sddm-hyprenv-theme folder.
* Ok tehre is cmd line that will do this, just change theme name, ok
```
sudo cp /usr/share/sddm/themes/sddm-hyprenv-theme/Themes/leaves.conf /usr/share/sddm/themes/sddm-hyprenv-theme/theme.conf
```
* Here leaves.conf is theme name, just changed that to the theme you want to have 


## Previewing a theme

You can preview the set theme without logging out by runnning:
```sh
sddm-greeter-qt6 --test-mode --theme /usr/share/sddm/themes/sddm-hyprenv-theme/
```
> Note that depending on the system configuration, the preview may differ slightly from the actual login screen.


Distributed under the **[GPLv3+](https://www.gnu.org/licenses/gpl-3.0.html) License**.    
Copyright (C) 2022-2025 Keyitdev.
