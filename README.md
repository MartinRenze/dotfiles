# dotfiles
.vimrc, .bashrc etc 

## Install
`git clone https://github.com/MartinRenze/dotfiles.git ~/.dotfiles`

`cd ~/.dotfiles && ./install.sh`


## Switch `Caps` and `Esc` Key
* `dconf write "/org/gnome/desktop/input-sources/xkb-options" "['caps:swapescape']"`
* done in script

## Switch `Y and Z` on German keyboard

* `sudo vim /usr/share/X11/xkb/symbols/de`
* Switch in first block 

## Shortcut Keys / Hotkeys
### Ubuntu
Key | Action
----|-------
`Strg` + `Alt` + `f` | Open Nautilus
`Strg` + `Alt` + `t` | Open Terminator
`Strg` + `Shift` + `print (prt sc)` | Select an area to take a screenshot and copy it to the clipboard
`Super` + `Tab` | Select window
`Super` + `Arrows` | Position window
`Super` + `Shift` + `Arrows` | Move window on different monitor

### Nautilus
`Strg` + `Shift` +`t` | Open new tab

### Terminator
`Strg` + `Shift` + `t` | Open new tab

### Bash
Key | Action
----|-------
`Strg` + `N` | Go one directory up (`cd ../`)

### Vim

### Linphone
* Config in `~/.config/linphone` and `~/.local/share/linphone`

### Update AppImages
* follow https://github.com/MartinRenze/update-appimage

### Tmux
Key | Action
----|-------
`Ctrl` + `b` then `[` | Open visual mode
`tmux a` | Attach to last session
`Ctrl` + `b` then `d` | Detach from session
`Ctrl` + `b` then `c` | Create new window

## Docker
* Allow docker to access `/media`
* `sudo snap connect docker:removable-media`
* Add user so we dont need sudo
* `sudo addgroup --system docker`
* `sudo adduser $USER docker`
* `newgrp docker`
* Exec into docker container
* `docker exec -it container_id bash`
* Run kali on docker
* `docker run --tty --interactive kalilinux/kali-rolling`
* `apt update && apt -y install kali-linux-headless`

## Disable webcam audio
* Create file `sudo vim /etc/udev/rules.d/90-block-webcam-sound.rules`
* find vendor und product id with `lsusb`
* with content:
```
# Do not want low quality webcam mic
SUBSYSTEM=="usb", DRIVER=="snd-usb-audio", ATTRS{idVendor}=="041e", ATTRS{idProduct}=="4097", ATTR{authorized}="0"
```
