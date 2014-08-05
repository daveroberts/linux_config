dwm
From here: http://cannibalcandy.wordpress.com/2012/04/26/installing-and-configuring-dwm-under-ubuntu/

```
sudo apt-get install build-essential libx11-dev libxinerama-dev sharutils suckless-tools
cd /usr/local/src
sudo wget http://dl.suckless.org/dwm/dwm-6.0.tar.gz
sudo tar xvzf dwm-6.0.tar.gz
chown -R `id -u`:`id -g` dwm-6.0
cd dwm-6.0
```

copy config.h from here to /usr/local/src/dwm-6.0

```
sudo make clean install
```

Install dwm official to get the option on login screen, copy it, then uninstall

```
sudo apt-get install dwm
sudo cp /usr/share/xsessions/dwm.desktop{,.bak}
sudo apt-get purge dwm
sudo mv /usr/share/xsessions/dwm.desktop{.bak,}
```

# Setup Console

console font: terminus 10
```
sudo apt-get install xfonts-terminus
```
Transparent background

Set "Run command as a login shell" to true

# Change background on dwm startup
```
sudo apt-get install feh
cd /usr/share/xsessions
sudo cp dwm.desktop dwm.desktop.orig
```
Change the Exec=dwm line to `Exec=/home/dave/.dwmstart`

```
touch ~/.dwmstart
chmod +x ~/.dwmstart
nano -w ~/.dwmstart
```

Add the following:
```bash
#! /bin/bash

sh ~/.fehbg &

exec dwm
```
Then `touch ~/.fehbg`

```
feh  --bg-scale '/home/dave/Pictures/YOUR_PRETTY_PICTURE_HERE.jpg'
```

# fish shell

install from source

install oh my zsh

gvim ~/.config/fish/config.fish

`set fish_plugins bundler rvm git`

# GVIM

`sudo apt-get install vim-gnome`

