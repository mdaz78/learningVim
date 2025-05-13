# Day 12: File Explorer Practice (netrw/tree)

## Goals:

- Master netrw, Vim's built-in file explorer
- Learn different ways to view and navigate directories
- Perform file operations efficiently

## Basic netrw Commands:

- `:Ex` - Open explorer in current window
- `:Sex` - Open explorer in horizontal split
- `:Vex` - Open explorer in vertical split
- `:Lex` - Open explorer in left window

## Navigation:

- `j/k` - Move up/down
- `Enter` - Open file/directory
- `-` - Go up directory
- `%` - Create new file
- `d` - Create new directory
- `D` - Delete file/directory
- `R` - Rename file/directory

## File Operations:

- `mf` - Mark file
- `mc` - Copy marked files
- `mm` - Move marked files
- `mx` - Execute command on marked files
- `mt` - Set target directory

## View Settings:

- `i` - Cycle through view types
- `gh` - Toggle hidden files
- `s` - Change sort order
- `r` - Reverse sort order

## Tree Plugin Features (if using nvim-tree):

- `:NvimTreeToggle` - Toggle tree view
- `:NvimTreeFindFile` - Find current file in tree
- `:NvimTreeCollapse` - Collapse all folders
- `:NvimTreeRefresh` - Refresh tree view

## Exercises:

1. Basic Navigation:

   - Open netrw with different commands
   - Navigate through directories
   - Toggle different view types
   - Show/hide hidden files

2. File Operations:

   - Create new files and directories
   - Rename and delete files
   - Mark multiple files
   - Perform operations on marked files

3. Split Views:
   - Use different split views
   - Navigate between splits
   - Organize files using split views

## Best Practices:

- Use marks for batch operations
- Learn keyboard shortcuts for efficiency
- Use appropriate split views for context
- Keep tree view organized

## Tips:

- Configure netrw settings in vimrc
- Use bookmarks for frequent directories
- Learn to preview files before opening
- Master split window navigation
