# nix

**Nix Installation Trail**

#how to update
sudo nix-channel --update && sudo nixos-rebuild switch && nix-env -u “*” && home-manager switch

#install vivaldi
sudo nix-channel --add https://nixos.org/channels/nixos-unstable nixos-unstable && echo ", vivaldi = pkgs.vivaldi;" | sudo tee -a /etc/nixos/configuration.nix && sudo nixos-rebuild switch



Arch XF Setup Installation Trail

station wlan0 connect "I Believe Why can Fhy(2.4)"

archinstall + vivaldi

sudo pacman -Rns --noconfirm xfce4-dict xfburn && sudo pacman -Syu --noconfirm --needed firefox yt-dlp linux-firmware pacman-contrib unzip lightdm-gtk-greeter-settings kcalc ksnip kdeconnect sshfs onboard spotify-launcher ibus picom xcompmgr smplayer qbittorrent baobab timeshift neofetch git && git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si --noconfirm && cd && sudo pacman-key --recv-key 3056513887B78AEB --keyserver keyserver.ubuntu.com && sudo pacman-key --lsign-key 3056513887B78AEB && sudo pacman -U --noconfirm 'https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-keyring.pkg.tar.zst' 'https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-mirrorlist.pkg.tar.zst' && echo -e "[chaotic-aur]\nInclude = /etc/pacman.d/chaotic-mirrorlist" | sudo tee -a /etc/pacman.conf && yay -S --needed --noconfirm --sudoloop --removemake realvnc-vnc-viewer google-chrome mugshot bibata-cursor-theme stremio peazip ventoy-bin stacer microsoft-edge-stable timeshift-autosnap normcap teamviewer zoom penguins-eggs mkinitcpio-openswap megasync && sudo sed -i 's/#Color/Color/' /etc/pacman.conf && sudo sed -i 's/#ParallelDownloads/ParallelDownloads/' /etc/pacman.conf && sudo sed -i '/Color/a ILoveCandy' /etc/pacman.conf && mkdir /home/$USER/Downloads && wget https://averagelinuxuser.com/assets/images/posts/2019-01-18-linux-terminal-color/Linux_terminal_color.zip && sudo mv /home/$USER/Linux_terminal_color.zip Downloads && cd Downloads && unzip Linux_terminal_color.zip && sudo mv bash.bashrc /etc/bash.bashrc && sudo mv DIR_COLORS /etc/ && mv .bashrc ~/.bashrc && cd && sudo systemctl enable paccache.timer && sudo rm /home/$USER/Downloads/Linux_terminal_color.zip -r yay && sudo pacman -Scc --noconfirm && sudo pacman -Rns --noconfirm $(pacman -Qtdq)

megasync + startup + thunar bookmarks +  panel + wallpapers + teamviewer + zoom + edge

startup: ksnip, kdeconnect-indicator

sudo eggs calamares -i && sudo eggs dad -d && sudo pacman -Syu --noconfirm && sudo pacman -Scc --noconfirm && sudo eggs tools skel && sudo eggs produce --clone
