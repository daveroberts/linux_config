dwm
From here: http://cannibalcandy.wordpress.com/2012/04/26/installing-and-configuring-dwm-under-ubuntu/
sudo apt-get install build-essential libx11-dev libxinerama-dev sharutils suckless-tools
cd /usr/local/src
sudo wget http://dl.suckless.org/dwm/dwm-6.0.tar.gz
sudo tar xvzf dwm-6.0.tar.gz
chown -R `id -u`:`id -g` dwm-6.0
cd dwm-6.0
copy config.h from here to /usr/local/src/dwm-6.0
sudo make clean install
Install dwm official to get the option on login screen, copy it, then uninstall
sudo apt-get install dwm
sudo cp /usr/share/xsessions/dwm.desktop{,.bak}
sudo apt-get purge dwm
sudo mv /usr/share/xsessions/dwm.desktop{.bak,}

console font: terminus 10
sudo apt-get install xfonts-terminus

background feh
sudo apt-get install feh
gvim .fehbg

fish
install from source
install oh my zsh
gvim ~/.config/fish/config.fish
set fish_plugins bundler rvm
