# dotfiles
.vimrc, .bashrc etc 

## Install
`git clone https://github.com/MartinRenze/dotfiles.git ~/.dotfiles`

`cd ~/.dotfiles && ./install.sh`


## Switch `Caps` and `Esc` Key

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

### Tmux
Key | Action
----|-------
`Ctrl` + `b` then `[` | Open visual mode
`tmux a` | Attach to last session
`Ctrl` + `b` then `d` | Detach from session
`Ctrl` + `b` then `c` | Create new window

## Docker
* Exec into docker container
* `docker exec -it container_id bash`
* Run kali on docker
* `docker run --tty --interactive kalilinux/kali-rolling`
* `apt update && apt -y install kali-linux-headless`
