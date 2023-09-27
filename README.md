**Nix Installation Trail**

#unstable channel
sudo nix-channel --add https://channels.nixos.org/nixos-unstable nixos

#confirm unstable channel
sudo nix-channel --list | grep nixos

#update and cleanup
sudo nixos-rebuild switch --repair && sudo nixos-rebuild switch --upgrade && sudo nix-collect-garbage -d && sudo nix-store --optimise && home manager switch

#open configuration file
sudo nano /etc/nixos/configuration.nix

#define hostname
#disable cups
#enable/disable touchpad support
#enable/disable ssh

#restore packages
#add these to the list after environment.systemPackages = with pkgs; [

pkgs.vivaldi
pkgs.wget
pkgs.teamviewer
pkgs.yt-dlp
pkgs.linux-firmware
pkgs.unzip
pkgs.kcalc
pkgs.ksnip
pkgs.sshfs
pkgs.onboard
pkgs.spotify
pkgs.ibus
pkgs.picom
pkgs.xcompmgr
pkgs.smplayer
pkgs.qbittorrent
pkgs.baobab
pkgs.borgbackup
pkgs.neofetch
pkgs.git
pkgs.realvnc-vnc-viewer
pkgs.google-chrome
pkgs.stremio
pkgs.ventoy-bin
pkgs.megasync
pkgs.xfce.xfce4-volumed-pulse
pkgs.xfce.xfce4-clipman-plugin
pkgs.xfce.xfce4-pulseaudio-plugin
pkgs.xfce4.xfce4-whiskermenu-plugin
pkgs.xfce.xfce4-panel-profiles
pkgs.microsoft-edge
pkgs.lightdm-gtk-greeter
pkgs.banana-cursor
pkgs.pavucontrol
pkgs.libsForQt5.kdeconnect-kde
pkgs.zoom-us
pkgs.rescuetime
pkgs.htop
#unstable-only packages
pkgs.stacer
pkgs.peazip
pkgs.normcap


#add these after “List services” but before the last “}” in the configuration file

“services.teamviewer.enable = true;

#keep NixOS system up-to-date automatically
system.autoUpgrade.enable = true;
system.autoUpgrade.allowReboot = true;”

#automatic nix store noontime garbage collection
nix.gc.automatic = true;
nix.gc.dates = "12:10";

#execute this command after
sudo nixos-rebuild switch

#figure out how to install/integrate later:
#mugshot 

megasync + startup + thunar bookmarks +  panel + wallpapers + teamviewer + zoom + edge

startup: ksnip, kdeconnect-indicator, megasync
