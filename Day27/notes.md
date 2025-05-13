# Day 27: Creating Your First Vim Plugin

## Goals:

- Learn plugin development basics
- Create a simple Neovim plugin
- Understand plugin structure
- Practice Lua plugin development

## Plugin Structure

### Basic Layout

```
~/.config/nvim/lua/my-plugin/
├── init.lua
├── utils.lua
└── config.lua
```

## Plugin Components

### init.lua - Main Entry Point

```lua
local M = {}

M.setup = function(opts)
    -- Plugin configuration
    opts = opts or {}
    vim.g.my_plugin_enabled = opts.enabled or true
end

return M
```

### utils.lua - Utility Functions

```lua
local M = {}

-- Word count function
M.count_words = function()
    local current_line = vim.api.nvim_get_current_line()
    local count = 0
    for word in current_line:gmatch("%S+") do
        count = count + 1
    end
    print("Words in line: " .. count)
end

-- Time stamp function
M.insert_timestamp = function()
    local time = os.date("%Y-%m-%d %H:%M:%S")
    local pos = vim.api.nvim_win_get_cursor(0)
    vim.api.nvim_buf_set_text(0, pos[1]-1, pos[2], pos[1]-1, pos[2], {time})
end

return M
```

## Creating Commands

### Command Registration

```lua
-- Create user commands
vim.api.nvim_create_user_command("CountWords", function()
    require("my-plugin.utils").count_words()
end, {})

vim.api.nvim_create_user_command("InsertTimestamp", function()
    require("my-plugin.utils").insert_timestamp()
end, {})
```

## Key Mappings

### config.lua - Keymaps Setup

```lua
local M = {}

M.setup_keymaps = function()
    vim.keymap.set('n', '<leader>cw',
        require("my-plugin.utils").count_words,
        { desc = "Count words in line" })

    vim.keymap.set('n', '<leader>ts',
        require("my-plugin.utils").insert_timestamp,
        { desc = "Insert timestamp" })
end

return M
```

## Plugin Development Best Practices

1. **Structure**

   - Keep code modular
   - Use local variables
   - Follow Lua conventions

2. **Documentation**

   - Write clear help docs
   - Document functions
   - Include examples

3. **Error Handling**

   - Use pcall for safety
   - Provide error messages
   - Handle edge cases

4. **Testing**
   - Write unit tests
   - Test edge cases
   - Manual testing

## Resources

### Documentation

- `:h writing-plugin` - Plugin writing guide
- `:h api` - Neovim API documentation
- `:h lua` - Lua reference

### Debugging

- `:lua require("my-plugin")` - Load plugin
- `:verbose map <leader>cw` - Check mapping
- `:LuaRepl` - Interactive Lua REPL
