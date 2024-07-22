# My bspwm

## Prerequisites

- [ ] bspwm
- [ ] dunst
- [ ] kitty terminal
- [ ] mpv
- [ ] nvim
- [ ] picom
- [ ] polybar
- [ ] rofi
- [ ] sxhkd
- [ ] zathura
- [ ] curl
- [ ] playerctl
- [ ] caffeine 

### Install dependencies 

```bash
sudo apt install bspwm dunst mpv nvim picom polybar rofi sxhkd zathura curl playerctl caffeine
```

### Kitty Terminal Installation

Run the next command:

```bash
curl -L https://sw.kovidgoyal.net/kitty/installer.sh | sh /dev/stdin
```
Then after the installation do this commands for desktop integration
https://sw.kovidgoyal.net/kitty/binary/#desktop-integration-on-linux


```bash
# Create symbolic links to add kitty and kitten to PATH (assuming ~/.local/bin is in
# your system-wide PATH)
ln -sf ~/.local/kitty.app/bin/kitty ~/.local/kitty.app/bin/kitten ~/.local/bin/
# Place the kitty.desktop file somewhere it can be found by the OS
cp ~/.local/kitty.app/share/applications/kitty.desktop ~/.local/share/applications/
# If you want to open text files and images in kitty via your file manager also add the kitty-open.desktop file
cp ~/.local/kitty.app/share/applications/kitty-open.desktop ~/.local/share/applications/
# Update the paths to the kitty and its icon in the kitty desktop file(s)
sed -i "s|Icon=kitty|Icon=$(readlink -f ~)/.local/kitty.app/share/icons/hicolor/256x256/apps/kitty.png|g" ~/.local/share/applications/kitty*.desktop
sed -i "s|Exec=kitty|Exec=$(readlink -f ~)/.local/kitty.app/bin/kitty|g" ~/.local/share/applications/kitty*.desktop
# Make xdg-terminal-exec (and hence desktop environments that support it use kitty)
echo 'kitty.desktop' > ~/.config/xdg-terminals.list
```

### Rofi addons

For enable the power menu please add this plugin to rofi
https://github.com/jluttine/rofi-power-menu

## NeoVim shortcuts

### Nav Tab
```
previous tab: [b
next tab: ]b
Horizontal split: \
Vertical split: |
Up window: ctrl + k
Down window: ctrl + j
Left window: ctrl + h
Right windor: ctrl + l
Resize up, down, left, right: ctrl + UP,DOWN,LEFT,RIGHT arrows

```

## Kitty Terminal

```
ctrl + shift + Enter: Split terminal in same tab
ctrl + shift + r: Resize windows inside layouts
```
