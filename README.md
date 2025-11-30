## Setup Guide

**Phase 1: Dependencies**
* **Font:** JetBrains Mono (Required)
* **Packages:** `pywal` `hyprpaper` `hypridle` `hyprlock` `waybar` `wlogout` `wofi` `nm-applet` `pavucontrol` `dunst` `nsxiv` `btop`

**Phase 2: Deployment**

**1. Clone & Prepare**
```bash
# Clone
git clone [https://github.com/phanthm/hyprland-dotfiles.git](https://github.com/phanthm/hyprland-dotfiles.git) && cd hyprland-dotfiles

# Create directories using brace expansion
mkdir -p ~/.config/{btop,dunst,gtk-3.0,gtk-4.0,hypr/scripts,kitty,wal/templates,waybar,wlogout,wofi}
mkdir -p ~/.local/share/icons/dunst
```

**2. Install Files**
```bash
cp -r config/* ~/.config/
cp -r local/* ~/.local/
cp .Xresources ~/
```

**Phase 3: Activation**

1.  **Trigger Wal:** Set your wallpaper using the switcher to generate the cache.
2.  **Symlink:** Run the following to link the generated colors:
    ```bash
    ln -sf ~/.cache/wal/dunstrc ~/.config/dunst/dunstrc
    ln -sf ~/.cache/wal/gtk4.css ~/.config/gtk-4.0/colors.css
    ln -sf ~/.cache/wal/colors-hyprland.conf ~/.config/hypr/colors.conf
    ```
