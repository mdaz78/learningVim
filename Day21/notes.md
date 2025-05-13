# Day 21: Vimscript and Lua Basics

## Goals:

- Learn basic Vimscript syntax
- Understand Lua integration
- Create basic configurations
- Set up custom mappings

## Basic Vimscript

### Commands and Variables

```vim
" Echo command
:echo "Hello World"

" Variables
:let name = "Vim"
:echo "Hello, " . name

" Functions
function! Greet(name)
    echo "Hello, " . a:name
endfunction

" Call with: :call Greet("User")
```

## Lua Basics

### Variables and Functions

```lua
-- Variables
local greeting = "Hello"
local count = 42

-- Functions
local function say_hello(name)
    print(string.format("%s, %s!", greeting, name))
end

-- Tables
local config = {
    theme = "dark",
    line_numbers = true,
    tab_width = 4
}
```

## Practical Configuration

### Vimscript Settings

```vim
" Basic settings
set number
set relativenumber
set expandtab
set tabstop=4
```

### Lua Settings

```lua
-- Basic settings
vim.opt.number = true
vim.opt.relativenumber = true
vim.opt.expandtab = true
vim.opt.tabstop = 4
```

## Key Mappings

### Vimscript Mappings

```vim
" Normal mode mapping
nnoremap <leader>ff :Files<CR>

" Visual mode mapping
vnoremap <leader>y "+y
```

### Lua Mappings

```lua
-- Normal mode mapping
vim.keymap.set('n', '<leader>ff', ':Files<CR>')

-- Visual mode mapping
vim.keymap.set('v', '<leader>y', '"+y')
```

## Best Practices

1. **Code Organization**

   - Keep related settings together
   - Use comments for sections
   - Modularize configurations

2. **Performance**

   - Use Lua for complex logic
   - Lazy load when possible
   - Profile startup time

3. **Maintainability**

   - Document custom functions
   - Use clear variable names
   - Follow consistent style

4. **Debugging**
   - Use :messages for output
   - Check :verbose map
   - Test configurations

## Quick Reference

### Vimscript

- `:echo` - Print output
- `:let` - Set variables
- `:function` - Define functions
- `:call` - Call functions

### Lua

- `:lua` - Execute Lua code
- `:luafile` - Source Lua file
- `:lua require()` - Load module
- `:lua print()` - Output text

### Integration

- `vim.cmd()` - Run Vim commands
- `vim.fn` - Call Vim functions
- `vim.api` - Use Vim API
- `vim.opt` - Set options
