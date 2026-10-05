# Hypr Wallpaper Manager

A bash script suite to manage your Steam Wallpaper Engine wallpapers on Linux (specifically suited for Hyprland/Wayland) using `linux-wallpaperengine`.

## Features
- Set, pause, and stop animated wallpapers.
- Built-in daemon for automatic wallpaper rotation (timer-based).
- Manage favorites and custom playlists.
- Interactive wallpaper selection using `fzf`.
- Global pause management across workspaces.

## Requirements
- `linux-wallpaperengine` (AUR)
- `jq`
- `bash`
- `fzf` (optional, for interactive selection)
- `libnotify` (optional, for notifications)

## Installation (Arch Linux)

You can install this package using an AUR helper like `yay` once the repository is pushed to GitHub:

```bash
yay -S hypr-wallpaper-manager-git
```

Alternatively, you can build it manually:

```bash
git clone https://github.com/FamilyTsuki/hypr-wallpaper-manager.git
cd hypr-wallpaper-manager
makepkg -si
```

## Usage

Check the help commands for each tool:
- `set-wallpaper --help`
- `wallpaper-add --help`
- `wallpaper-daemon --help`
