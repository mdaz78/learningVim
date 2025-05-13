# Day 10: Buffer and Window Management

## Goals:

- Learn to manage multiple buffers effectively
- Master window splitting and navigation
- Understand buffer vs window concepts

## Buffer Management:

- `:ls` - List all buffers
- `:b1`, `:b2`, etc. - Switch to buffer by number
- `:bn` - Go to next buffer
- `:bp` - Go to previous buffer
- `:bd` - Delete (close) current buffer

## Window Management:

- `:sp` or `Ctrl-w s` - Split window horizontally
- `:vsp` or `Ctrl-w v` - Split window vertically
- `Ctrl-w h/j/k/l` - Navigate between windows
- `Ctrl-w +/-/</>` - Resize windows
- `:q` - Close current window

## Window Resizing:

- `Ctrl-w +` - Increase height
- `Ctrl-w -` - Decrease height
- `Ctrl-w >` - Increase width
- `Ctrl-w <` - Decrease width
- `Ctrl-w =` - Make all windows equal size

## Additional Commands:

- `Ctrl-w o` - Make current window the only one (close others)
- `:b name` - Switch to buffer by name
- `:bd` - Delete current buffer
- `:ls` - Show buffer list with details

## Exercises:

1. Buffer Navigation:

   - List all buffers with `:ls`
   - Switch between buffers using `:b1`, `:bn`, `:bp`
   - Delete unused buffers with `:bd`

2. Window Management:

   - Create horizontal and vertical splits
   - Navigate between windows using `Ctrl-w` commands
   - Resize windows using various commands
   - Practice closing individual windows vs all windows

3. Combined Practice:
   - Open multiple buffers in different windows
   - Arrange windows in various layouts
   - Navigate efficiently between buffers and windows
