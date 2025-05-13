# Day 24: Terminal Usage in Neovim

## Goals:

- Master terminal integration in Neovim
- Learn terminal navigation
- Manage multiple terminals
- Create efficient workflows

## Basic Terminal Commands

### Opening Terminals

- `:terminal` - Open terminal in current window
- `:vertical terminal` - Open in vertical split
- `:horizontal terminal` - Open in horizontal split

### Common Terminal Commands

```bash
$ ls -la    # List files with details
$ pwd       # Print working directory
$ echo $PATH # Show PATH variable
$ ps aux | grep vim # Check vim processes
```

## Terminal Navigation

### Mode Switching

- `Ctrl-\ Ctrl-n` - Enter normal mode
- `i` or `a` - Enter terminal mode
- `Ctrl-w w` - Switch windows
- `Ctrl-w c` - Close terminal

### Example Workflow

1. Edit code
2. Run tests in terminal
3. Switch back to code
4. Repeat

## Multiple Terminals

### Terminal Types

1. Shell terminal (`:term zsh`)
2. Node REPL (`:term node`)
3. Python REPL (`:term python3`)

### Layout Example

```
+-------------+-------------+
|    Code     |   Shell    |
|             |            |
+-------------+-------------+
|    Tests    |    Logs    |
|             |            |
+-------------+-------------+
```

## Terminal Integration

### Running Files

```vim
:term node %      " Run current file with Node
:term python3 %   " Run with Python
```

### Testing Commands

```vim
:term npm test
:term python -m pytest
```

### Git Operations

```vim
:term git status
:term git log
```

## Best Practices

1. **Terminal Organization**

   - Keep related terminals grouped
   - Use meaningful names
   - Close unused terminals

2. **Workflow Optimization**

   - Use split layouts effectively
   - Keep test terminal visible
   - Automate common commands

3. **Navigation Tips**

   - Learn terminal mode shortcuts
   - Use window navigation commands
   - Master mode switching

4. **Common Patterns**
   - Editor + Terminal
   - Multiple REPLs
   - Test + Output
   - Build + Logs

## Quick Reference

### Terminal Commands

- `:term` - Open terminal
- `:bd!` - Force close terminal
- `Ctrl-\ Ctrl-n` - Exit terminal mode
- `Ctrl-w N` - Terminal normal mode
- `:terminal {cmd}` - Run specific command

### Navigation

- `Ctrl-w h/j/k/l` - Move between splits
- `Ctrl-w H/J/K/L` - Move terminal window
- `Ctrl-w =` - Equal size splits
- `Ctrl-w _` - Maximize height
- `Ctrl-w |` - Maximize width
