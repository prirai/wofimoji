# wofimoji

Emoji picker for wayland compositors using wofi.

*Part of my dotfiles repository at* - [prirai/dotfiles](https://github.com/prirai/dotfiles)

## Prerequisites

Make sure you have `wofi` already installed.

## Installation

* Auto-installation:
  
  * Clone the repository:
    
    ```bash
    git clone https://github.com/prirai/wofimoji.git
    ```
  
  * Run the install script with:
    
    ```bash
    ./install.sh
    ```
- Manual copy-pasting:
  
  - Use your editor of choice to edit the file at `~/.local/bin/wofimoji`. Here I'm using nano. `nano ~/.local/bin/wofimoji`
  
  - Paste the contents of the `wofimoji` file into it.
  
  - Make the file executable: `chmod +x ~/.local/bin/wofimoji`

## Usage

In the config file for sway, add these two lines:

```
set $emoji-sel wofimoji
bindsym $mod+period exec $emoji-sel
```

Don't forget to add ~/.local/bin to `$PATH`. You can do this by editing either your bash, zsh or fish config or by editing `/etc/environment`.

Reload sway using `mod+Shift+C`. Pressing `mod+.` now brings up the wofimoji selector.
