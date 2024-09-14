echo " "
echo "Would you like to install the Fluorine desktop?"
echo "If so, respond by pressing "y" then hitting enter."
echo "If not, please respond with anything other than that."
read -p "Do you want to continue [y/n]: " prompt
if [[ $prompt == y* ]]; then
	cd ~
	clear
	sudo pacman -S rsync git lxappearance-obconf lxterminal xorg-xrdb tint2 openbox jgmenu xwallpaper xorg-xinit thunar tumbler cantarell-fonts 	obconf xorg-server gnu-free-fonts polkit l3afpad
	git clone https://github.com/vinceliuice/Qogir-icon-theme
	mkdir -p ~/.local/share/icons; ./Qogir-icon-theme/install.sh -d ~/.local/share/icons -c all
	mkdir .themes
	mkdir ~/Desktop
	mkdir ~/Documents
	mkdir ~/Downloads
	mkdir ~/Music
	mkdir ~/Pictures
	mkdir ~/Videos
	git clone -b Material-Black-Colors-Desktop https://github.com/rtlewis1/GTK.git
	cp -R GTK/* ~/.themes/
	git clone https://github.com/4194304/fluorine-desktop
	rsync -av fluorine-desktop/ ~
 	curl -O https://github.com/manu-mannattil/adwaita-cursors/releases/download/v1.2/adwaita-cursors.tar.gz
	tar xvzf adwaita-cursors.tar.gz
	mkdir -p ~/.icons/default
	mv adwaita-cursors/Adwaita/cursors ~/.icons/default
	rm -rf fluorine-desktop Qogir-icon-theme GTK screenshot.png LICENSE README.md fluorine-settings adwaita-cursors
	chmod +x ~/.fluorine/*
 	cp ~/.local/share/icons/Qogir/scalable/apps/file-manager.svg ~/.local/share/icons/Qogir/scalable/apps/org.xfce.thunar.svg
  	cp ~/.local/share/icons/Qogir/scalable/apps/org.xfce.terminal.svg ~/.local/share/icons/Qogir/scalable/apps/lxterminal.svg
	echo " "
	sed -i "s/fluorine/$USER/g" ~/.config/gtk-3.0/bookmarks
	echo "Installation complete!"
	echo "If you would like to start Fluorine (if in a TTY), run startx."
	exit
else
    echo "Stopping!"
    exit
fi
