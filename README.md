# tmux config

Personal tmux configuration with vim-style keybindings, Catppuccin theme, and quality-of-life improvements.

## Installation

Plugins are managed by [TPM](https://github.com/tmux-plugins/tpm). After cloning, install plugins with:

```
prefix + I
```

## Prefix

The prefix is remapped from the default `Ctrl-b` to **`Ctrl-a`**.

## Keybindings

### General

| Key          | Action        |
| ------------ | ------------- |
| `prefix + r` | Reload config |

### Pane Management

| Key          | Action                                          |
| ------------ | ----------------------------------------------- |
| `prefix + v` | Split pane vertically (opens in current path)   |
| `prefix + s` | Split pane horizontally (opens in current path) |
| `prefix + m` | Toggle pane zoom (maximize/restore)             |

### Pane Navigation (vim-style)

| Key          | Action             |
| ------------ | ------------------ |
| `prefix + h` | Move to pane left  |
| `prefix + j` | Move to pane below |
| `prefix + k` | Move to pane above |
| `prefix + l` | Move to pane right |

### Pane Resizing (repeatable)

| Key          | Action            |
| ------------ | ----------------- |
| `prefix + H` | Resize pane left  |
| `prefix + J` | Resize pane down  |
| `prefix + K` | Resize pane up    |
| `prefix + L` | Resize pane right |

Resize keys are repeatable — hold `prefix` and tap the resize key multiple times without re-pressing prefix.

### Copy Mode (vim-style)

Enter copy mode with `prefix + [`, then:

| Key      | Action                            |
| -------- | --------------------------------- |
| `v`      | Begin selection                   |
| `Ctrl-v` | Toggle rectangle selection        |
| `y`      | Copy selection and exit copy mode |

Mouse drag does **not** auto-copy — use `y` to copy explicitly.

## Mouse Support

Mouse is enabled. You can click to focus panes, scroll history, and resize panes by dragging borders.

## Other Settings

- **Clipboard**: System clipboard integration is on (`set-clipboard on`)
- **Colors**: Full RGB/true color support via `tmux-256color` and terminal overrides
- **Window numbering**: Starts at 1 (not 0); windows renumber automatically when one is closed
- **Window renaming**: Automatic rename is disabled — window names stay as you set them

## Plugins

| Plugin                                                | Purpose                         |
| ----------------------------------------------------- | ------------------------------- |
| [tpm](https://github.com/tmux-plugins/tpm)            | Plugin manager                  |
| [catppuccin/tmux](https://github.com/catppuccin/tmux) | Status bar theming (Catppuccin) |

The status bar shows the current window name with a icon.
