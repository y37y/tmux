# Tmux Configuration for Ubuntu

My tmux terminal multiplexer configuration optimized for Ubuntu/Debian systems.

## Installation

1. Install tmux:
```bash
brew install tmux
```

2. Clone the repository:
```bash
git clone https://github.com/y37y/tmux.git ~/.config/tmux
```

3. Install Tmux Plugin Manager (TPM):
```bash
git clone https://github.com/tmux-plugins/tpm ~/.config/tmux/plugins/tpm
```

4. Install plugins:
- Start tmux: `tmux`
- Press `Alt+a` then `I` (capital i) to install plugins

## Features

### General Settings
- Custom prefix key (Alt-a)
- Vi mode keybindings
- Mouse support
- Extended color support (256 colors)
- Increased history limit (1,000,000 lines)
- Zero escape time
- Focus events enabled

### Plugins
- `tmux-plugins/tpm`: Plugin manager
- `tmux-plugins/tmux-sensible`: Sensible defaults
- `tmux-plugins/tmux-yank`: Clipboard integration
- `tmux-plugins/tmux-prefix-highlight`: Prefix indicator
- `tmux-plugins/tmux-resurrect`: Session saving
- `tmux-plugins/tmux-continuum`: Automatic session saving
- `catppuccin/tmux`: Theme (Mocha flavor)
- `wfxr/tmux-fzf-url`: URL handling
- `omerxx/tmux-sessionx`: Session management

### Key Bindings

#### Window Management
- `Alt+b`: Break pane into window
- `Alt+o`: Kill all panes except current
- `Alt+q`: Kill window
- `Alt+e`: Kill all windows except current
- `Alt+[/]`: Previous/next window
- `H/L`: Previous/next window
- `prefix + r`: Rename window
- `prefix + R`: Reload configuration

#### Pane Management
- `prefix + |/v`: Split vertically
- `prefix + -/s`: Split horizontally
- `prefix + z`: Toggle pane zoom
- `prefix + h/j/k/l`: Navigate panes
- `prefix + x`: Swap pane
- `prefix + P`: Toggle pane border status

#### Copy Mode (Vi)
- `Alt+c`: Enter copy mode
- `v`: Begin selection
- `C-v`: Rectangle toggle
- `h/j/k/l`: Move cursor
- `y`: Copy selection
- `Y`: Copy line
- `?`: Search reverse

#### Vim Integration
Smart pane navigation when using Vim:
- `C-h/j/k/l`: Navigate panes
- `C-Left/Right/Up/Down`: Resize panes

## Configuration Files
- `tmux.conf`: Main configuration file
- `tmux.reset.conf`: Reset configuration

## Theme
Using Catppuccin Mocha theme with:
- Status bar at top
- Custom window status style
- Custom status line format
- Custom colors for active/inactive panes

## Additional Features
- Automatic session restore
- NeoVim session support
- URL handling with fzf
- Extended key support
- System clipboard integration

## Key Commands
- Reload config: `prefix + R`
- List windows: `prefix + w`
- Choose session: `prefix + S`
- Clear screen: `prefix + K`
- Toggle synchronized panes: `prefix + *`
