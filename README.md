# sddm-hyprenv-theme :

|![image](https://github.com/user-attachments/assets/d952c52e-bf3f-46a5-90b7-5273aec67506)|![image](https://github.com/user-attachments/assets/3e784692-4286-4500-a68f-cfe52eface74)|
|---|---|

It's written using the latest version of Qt, which is **Qt6**. This theme also support **animated wallpapers**. You can easily change its appearance by choosing another of the 5 pre-made themes or creating your own.

> [!NOTE]
> All themes were created for 1080p. However, they should work well in other resolutions.



## Installation :

1. Install **dependencies**

**Arch Linux** - 
```
sudo pacman -S --needed sddm qt6-svg qt6-virtualkeyboard qt6-multimedia-ffmpeg qt6-quickeffectmaker
```

**Others Linux Distros** -
```sh
sddm qt6-svg qt6-virtualkeyboard qt6-multimedia            # Void
sddm qt6-qtsvg qt6-qtvirtualkeyboard qt6-qtmultimedia      # Fedora
sddm-qt6 libQt6Svg6 qt6-virtualkeyboard qt6-virtualkeyboard-imports qt6-multimedia qt6-multimedia-imports        # OpenSUSE
sddm libqt6svg6 qt6-virtualkeyboard-plugin libqt6multimedia6 qml6-module-qtquick-controls qml6-module-qtquick-effects # Debian Unstable
```

2. Clone repository
```
git clone https://github.com/Ayu-0/sddm-hyprenv-theme.git
```
3. Copy theme to `/usr/share/sddm/themes/`
```
sudo cp -r sddm-hyprenv-theme /usr/share/sddm/themes
```
4. Copy fonts to `/usr/share/fonts/`
```
sudo cp -r /usr/share/sddm/themes/sddm-hyprenv-theme/Fonts/* /usr/share/fonts/ && sudo fc-cache -fv
```
5. Create a file `theme.conf` inside `/etc/sddm.conf.d`, If directory not exits then create it by running
```
sudo mkdir -p /etc/sddm.conf.d
```
```
sudo nano /etc/sddm.conf.d/theme.conf
```
6. Add the following contents to theme.conf
```
[Theme]
Current=sddm-hyprenv-theme
```
8. Create `virtualkbd.conf` file to `/etc/sddm.conf.d/` & add following contents
```sh
[General]
InputMethod=qtvirtualkeyboard"
```

## Selecting a theme

* By default `purple-heart` theme is active, active theme is managed by a file named `theme.conf` inside the `sddm-hyprenv-theme` directory
* So, If you want to change the theme, all you have to do is :
  - Go to the `Themes/` directory inside the `sddm-hyprenv-theme` folder.
  - Pick your desired theme file (e.g., `leaves.conf`)
  - Rename it to `theme.conf` and move or copy it to the `sddm-hyprenv-theme` folder.
* You don't have to do it manually — just run the following command and replace `leaves` with your `theme name`:
```
sudo cp /usr/share/sddm/themes/sddm-hyprenv-theme/Themes/leaves.conf /usr/share/sddm/themes/sddm-hyprenv-theme/theme.conf
```
**Available Themes** :
-  purple-heart
-  outer-wilds
-  leaves
-  the-view
-  forest

## Previewing a theme

You can preview the set theme without logging out by runnning:
```sh
sddm-greeter-qt6 --test-mode --theme /usr/share/sddm/themes/sddm-hyprenv-theme/
```
> Note that depending on the system configuration, the preview may differ slightly from the actual login screen.

