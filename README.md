**Nix Installation Trail**

#update and cleanup
sudo nixos-rebuild switch --repair && sudo nix-collect-garbage -d && sudo nixos-rebuild switch --upgrade && home-manager switch

#unstable channel
sudo nix-channel --add https://channels.nixos.org/nixos-unstable nixos


#open configuration file
sudo nano /etc/nixos/configuration.nix

#define hostname
#disable cups
#enable touchpad support
#enable ssh

#restore packages
#add these to the list after environment.systemPackages = with pkgs; [

 (vivaldi.override {
    proprietaryCodecs = true;
    enableWidevine = true;
  })
  vivaldi-ffmpeg-codecs
  widevine-cdm
  wget
  teamviewer
  yt-dlp
  linux-firmware
  unzip
  kcalc
  ksnip
  sshfs
  onboard
  spotify
  ibus
  picom
  xcompmgr
  smplayer
  qbittorrent
  baobab
  timeshift
  neofetch
  git
  realvnc-vnc-viewer
  google-chrome
  stremio
  ventoy-bin
  megasync
  pkgs.xfce.xfce4-volumed-pulse
  pkgs.xfce.xfce4-clipman-plugin
  pkgs.xfce.xfce4-pulseaudio-plugin
  pkgs.xfce.xfce4-whiskermenu-plugin
  pkgs.microsoft-edge
  pkgs.lightdm-gtk-greeter
  pkgs.bibata-cursors
  pkgs.pavucontrol
  pkgs.libsForQt5.kdeconnect-kde
  pkgs.zoom-us
  pkgs.rescuetime
  pkgs.htop
  #unstable packages
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
#mugshot timeshift-autosnap 

megasync + startup + thunar bookmarks +  panel + wallpapers + teamviewer + zoom + edge

startup: ksnip, kdeconnect-indicator, megasync

#deep clean & shutdown
sudo nix-store --optimise && sudo poweroff
