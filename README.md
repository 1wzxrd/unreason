readme.

secure blazing peformative (c/rust/shell workflow).
low overhead, clean policy, anti bloat, private, minimal


archetecture = void x11 ( base live image ) glibc x86_64


full list = dwm, dmenu, st, slock,dblock, xresources, systray, systray-toggle, statuscmd, wintitle, walrs, xcompmgr, xwallpaper, dunst, gammastep, light, seatd, dbus, xorg-server, xinit, mesa, maim, clipmenu, iwd, impala, bluez, bluetuith, xzoom, xfe, pipewire, lsp-plugin, rnnoise, libpipewire-module-filter-chain, pavucontrol, pipewire-pulse, wireplumber, limits.conf(rtprio&memlock, ncpamixer(ncurser),nano, xtools,













# unreason 

A reproducible Void Linux (glibc) X11 desktop setup built around dwm, st, dmenu, walrs, and xwallpaper on the `static` branch.

## Structure

Every `unreason` `static` checkout follows this layout:

unreason/
  dotfiles/
    shell/
      xinitrc
      zshrc
      zprofile
      fastfetch/
      btop/
    script/
      snap
      set-wallpaper
    theme/
      xwallpaper/
      walrs/
      xfe/
      fonts/
    suckless/
      dmenu/
        bar.sh
        launcher.sh
      dwm/
        dwm.c
        config.h
        colors.h
      st/
        config.h
      slstatus/
        config.h
        arg.h
      slock/
        config.h
  README.md

## The manifest

[meta]
name = "unreason"
author = "1wzxrd"
branch = "static"
wm = "dwm"
display_server = ["x11"]
colorscheme = "walrs"
components = ["dwm", "st", "dmenu", "slstatus", "slock", "dunst"]
description = "Reproducible Void glibc dwm and st setup with walrs and xwallpaper"

[dependencies]
packages = ["base-devel", "libX11-devel", "libXft-devel", "libXinerama-devel", "fontconfig-devel", "xwallpaper", "dmenu", "slock", "zsh", "btop", "fastfetch", "walrs"]
fonts = ["CozetteVector"]

[wallpaper]
link = "~/.config/wallpaper.jpg"
setter = "xwallpaper"
theme_generator = "walrs"
