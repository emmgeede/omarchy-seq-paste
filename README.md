# omarchy-seq-paste

Sequential copy/paste (FIFO clipboard) for Hyprland, inspired by macOS [Pastebot](https://tapbots.com/pastebot/). Designed for [Omarchy](https://github.com/basecamp/omarchy).

Copy multiple items in sequence, then paste them back in the same order. A floating panel shows the current queue.

## Install

```bash
yay -S omarchy-seq-paste
```

Or build manually:

```bash
git clone https://aur.archlinux.org/omarchy-seq-paste.git
cd omarchy-seq-paste
makepkg -si
```

## Setup

Add these lines to your Hyprland config (e.g. `~/.config/hypr/hyprland.conf`):

```conf
source = /usr/share/omarchy-seq-paste/hyprland-rules.conf
source = /usr/share/omarchy-seq-paste/hyprland-bindings.conf
```

The default keybindings use `SUPER+ALT+C/V/X`. To use different modifiers, copy the bindings file and edit it:

```bash
cp /usr/share/omarchy-seq-paste/hyprland-bindings.conf ~/.config/hypr/seq-paste-bindings.conf
# Edit to taste, then source your local copy instead
```

## Usage

| Action | Default Binding | Command |
|--------|----------------|---------|
| Copy to queue | `Super+Alt+C` | `omarchy-seq-paste push` |
| Paste from queue | `Super+Alt+V` | `omarchy-seq-paste paste` |
| Clear queue | `Super+Alt+X` | `omarchy-seq-paste clear` |

The panel opens automatically when items are queued and closes when the queue is empty.

## Dependencies

- `wl-clipboard` — Wayland clipboard access
- `inotify-tools` — live panel updates
- `ghostty` — terminal for the floating panel
- `libnotify` — desktop notifications
- `hyprland` — window manager (for `hyprctl`)

## License

MIT
