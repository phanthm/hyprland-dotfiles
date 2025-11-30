## Setup Guide

### **Prerequisites**
* **Font:** JetBrains Mono
* **Packages:** `pywal` `hyprpaper` `hypridle` `hyprlock` `waybar` `wlogout` `wofi` `nm-applet` `pavucontrol` `dunst` `nsxiv` `btop`

### **Installation**

**Clone**
```bash
git clone https://github.com/phanthm/hyprland-dotfiles.git && cd hyprland-dotfiles
```

**Copy Files**
```bash
# Create directories 
mkdir -p ~/.config/{btop,dunst,gtk-3.0,gtk-4.0,hypr/scripts,kitty,wal/templates,waybar,wlogout,wofi}
mkdir -p ~/.local/share/icons/dunst

# Copy
cp -r config/* ~/.config/
cp -r local/* ~/.local/
cp .Xresources ~/
```

**Trigger Wal:** 
Set a wallpaper using the switcher once to generate the cache.

**Symlink:** 
Link the generated colors/config:
```bash
ln -sf ~/.cache/wal/dunstrc ~/.config/dunst/dunstrc
ln -sf ~/.cache/wal/gtk4.css ~/.config/gtk-4.0/colors.css
ln -sf ~/.cache/wal/colors-hyprland.conf ~/.config/hypr/colors.conf
```

**NOTE**: Before compiling nsxiv, add these lines to the config.h file in the keys[] array to select the wallpaper using Enter and exit with Esc:
```
{ 0,            XK_Return,        g_pick_quit,          0 },
{ 0,            XK_Escape,        g_quit,               0 },
```
