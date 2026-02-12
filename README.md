# Tmux Configuration

A modern, keyboard-driven tmux configuration optimized for:

* Ubuntu / Debian
* macOS
* SSH-heavy workflows
* Vim / Neovim users
* Long-running sessions & development environments

This setup follows the **XDG directory layout** and keeps plugins managed by TPM (not versioned in this repo).

---

# Installation

## 1. Install tmux

### Ubuntu / Debian

```bash
sudo apt update
sudo apt install tmux
```

### macOS

```bash
brew install tmux
```

---

## 2. Clone this repository

```bash
git clone https://github.com/y37y/tmux.git ~/Projects/tmux
```

This repository contains only configuration files — plugins are installed separately.

---

## 3. Symlink into `~/.config`

This configuration follows the XDG standard:

```bash
mkdir -p ~/.config
ln -sfn ~/Projects/tmux ~/.config/tmux
ln -sfn ~/.config/tmux/tmux.conf ~/.tmux.conf
```

This makes:

```
~/Projects/tmux        → source of truth (git repo)
~/.config/tmux         → runtime config directory
~/.tmux.conf           → entrypoint for tmux
```

---

## 4. Install Tmux Plugin Manager (TPM)

Plugins are **not tracked in this repository**.

Install TPM:

```bash
git clone https://github.com/tmux-plugins/tpm ~/.config/tmux/plugins/tpm
```

---

## 5. Install Plugins

Start tmux:

```bash
tmux
```

Then press:

```
Alt + a    then    Shift + I
```

If Meta/Alt does not work (common over SSH on macOS):

```
Esc    a    Shift + I
```

TPM will clone and install all configured plugins.

---

# Features

## Core Settings

* Custom prefix: `Alt + a` (Meta-a)
* Vi keybindings in copy mode
* Mouse support enabled
* 256-color support
* 1,000,000 line scrollback history
* Zero escape delay
* Focus event support
* Status bar positioned at the top
* Pane indexing starts at 1

---

# Plugins

Managed via TPM:

* `tmux-plugins/tpm` – Plugin manager
* `tmux-plugins/tmux-sensible` – Sensible defaults
* `tmux-plugins/tmux-yank` – Clipboard integration
* `tmux-plugins/tmux-prefix-highlight` – Prefix indicator
* `tmux-plugins/tmux-resurrect` – Save/restore sessions
* `tmux-plugins/tmux-continuum` – Automatic session saving
* `catppuccin/tmux` – Mocha theme
* `wfxr/tmux-fzf-url` – URL extraction
* `omerxx/tmux-sessionx` – Session navigation
* `fcsonline/tmux-thumbs` – Jump to visible text
* `sainnhe/tmux-fzf` – Fuzzy navigation

---

# Key Bindings

## Prefix

```
Alt + a
```

If Meta is unreliable:

```
Esc, then a
```

---

## Window Management

| Action                 | Key          |
| ---------------------- | ------------ |
| New window             | `prefix + a` |
| Kill window            | `Alt + q`    |
| Kill all other windows | `Alt + e`    |
| Previous window        | `Alt + [`    |
| Next window            | `Alt + ]`    |
| Rename window          | `prefix + r` |
| Reload config          | `prefix + R` |

---

## Pane Management

| Action              | Key                |   |
| ------------------- | ------------------ | - |
| Split vertical | `Alt+a` then `|` |
| Split horizontal    | `prefix + -`       |   |
| Zoom pane           | `prefix + z`       |   |
| Navigate panes      | `prefix + h/j/k/l` |   |
| Swap pane           | `prefix + x`       |   |
| Toggle pane borders | `prefix + P`       |   |

---

## Copy Mode (Vi Style)

| Action           | Key        |
| ---------------- | ---------- |
| Enter copy mode  | `Alt + c`  |
| Begin selection  | `v`        |
| Rectangle select | `Ctrl + v` |
| Copy selection   | `y`        |
| Copy line        | `Y`        |
| Reverse search   | `?`        |

---

## Vim Integration

Smart navigation when inside Vim/Neovim:

```
Ctrl + h/j/k/l
```

Pane resizing:

```
Ctrl + Arrow keys
```

---

# Configuration Files

* `tmux.conf` – Main configuration
* `tmux.reset.conf` – Keybinding reset layer

---

# Useful Commands

Reload config:

```bash
prefix + R
```

List sessions:

```bash
prefix + S
```

Clear screen:

```bash
prefix + K
```

Toggle synchronized panes:

```bash
prefix + *
```

---

# Updating Plugins

Update all plugins:

```
prefix + U
```

Clean unused plugins:

```
prefix + Alt + u
```

