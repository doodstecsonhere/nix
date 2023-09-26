Nix Installation Trail

#update and cleanup
sudo nix-channel --update && sudo nixos-rebuild switch && nix-env -u ‘*’ && home-manager switch && nix-store --gc && nix-store --gc --delete-orphans && nix-env --clean

#add unstable repo
???

#open configuration file
sudo nano /etc/nixos/configuration.nix

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
  #unstable packages to install later
  #pkgs.stacer
  #pkgs.peazip
  #pkgs.normcap
 
#add this before the last “}” in the configuration file
services.teamviewer.enable = true;

#execute this command after
sudo nixos-rebuild switch

#figure out how to install/integrate later:
#mugshot timeshift-autosnap 

megasync + startup + thunar bookmarks +  panel + wallpapers + teamviewer + zoom + edge

startup: ksnip, kdeconnect-indicator, megasync
