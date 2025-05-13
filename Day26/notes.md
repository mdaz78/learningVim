# Day 26: tmux + Vim Integration

## Goals:

- Learn tmux basics
- Integrate tmux with Vim
- Master split pane workflows
- Configure seamless navigation

## Basic tmux Commands

### Session Management

- `tmux new -s vim-session` - Create new session
- `tmux ls` - List sessions
- `tmux attach -t vim-session` - Attach to session
- `Prefix + d` - Detach from session

### Window Operations

- `Prefix + c` - Create new window
- `Prefix + n` - Next window
- `Prefix + p` - Previous window
- `Prefix + &` - Kill window

### Pane Management

- `Prefix + %` - Split vertically
- `Prefix + "` - Split horizontally
- `Prefix + x` - Kill pane
- `Prefix + space` - Next layout

## Vim-tmux Navigation

### Movement Between Panes

- `Ctrl-h` - Move left
- `Ctrl-j` - Move down
- `Ctrl-k` - Move up
- `Ctrl-l` - Move right

### Common Layout

```
+----------------+----------------+
|                |                |
|      Vim       |    Terminal    |
|                |                |
+----------------+----------------+
|                |                |
|      Tests     |      Logs      |
|                |                |
+----------------+----------------+
```

## Copy-Paste Integration

### Vim to tmux

1. Visual select in Vim
2. Yank to system clipboard
3. Paste in tmux

### tmux to Vim

1. Enter copy mode (`Prefix + [`)
2. Select text
3. Copy to buffer (`Enter`)
4. Paste in Vim

## Configuration

### tmux.conf Example

```conf
# Smart pane switching
bind -n C-h select-pane -L
bind -n C-j select-pane -D
bind -n C-k select-pane -U
bind -n C-l select-pane -R

# Enable mouse mode
set -g mouse on

# Vim-like copy mode
setw -g mode-keys vi
```

## Advanced Integration

### Features

1. Send commands to pane
2. Run tests in split
3. View git status
4. Monitor logs

### Best Practices

- Use consistent keybindings
- Keep related panes grouped
- Leverage session management
- Name windows meaningfully

## Tips and Tricks

1. **Session Management**

   - Name sessions descriptively
   - Use different sessions per project
   - Save session layouts

2. **Window Organization**

   - Group related windows
   - Use meaningful names
   - Keep common layouts

3. **Pane Workflows**

   - Editor + Terminal
   - Tests + Output
   - Logs + Monitoring

4. **Performance**
   - Limit number of panes
   - Clean up unused sessions
   - Monitor resource usage
