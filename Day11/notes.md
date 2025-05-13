# Day 11: Understanding Tabs vs Buffers

## Goals:

- Understand the difference between tabs and buffers in Vim
- Master tab management
- Learn efficient buffer organization within tabs

## Tab Management:

- `:tabnew` - Create a new tab
- `gt` - Go to next tab
- `gT` - Go to previous tab
- `{n}gt` - Go to tab number n
- `:tabs` - List all tabs
- `:tabc` - Close current tab
- `:tabo` - Close all other tabs
- `:tabm N` - Move tab to position N

## Buffer Management:

- `:ls` - List all buffers
- `:b{n}` - Switch to buffer n
- `:bn` - Next buffer
- `:bp` - Previous buffer
- `:bd` - Delete current buffer

## Tabs vs Buffers:

### Tabs:

- Represent different window layouts
- Useful for different workspace contexts
- Can contain multiple windows/buffers
- More visual organization

### Buffers:

- Hold the actual file contents
- Can be hidden or visible
- More memory efficient
- Can be displayed in any window/tab

## Best Practices:

1. Use buffers for:

   - Working with related files
   - Quick switching between files
   - Memory efficient file management

2. Use tabs for:
   - Different workspace contexts
   - Organizing different aspects of work
   - Visual separation of tasks

## Exercises:

1. Tab Management:

   - Create multiple tabs with `:tabnew`
   - Navigate between tabs with `gt` and `gT`
   - Move tabs around with `:tabm`
   - Practice closing individual and other tabs

2. Buffer Organization:

   - Open multiple files into buffers
   - List and navigate buffers
   - Delete unused buffers
   - Switch between buffers in different ways

3. Combined Workflows:
   - Open multiple buffers in different tabs
   - Create split windows within tabs
   - Practice efficient navigation between all views
