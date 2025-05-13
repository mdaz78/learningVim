# Day 28: VSCodeVim and IdeaVim Configuration

## Goals:

- Configure VSCodeVim effectively
- Set up IdeaVim for IntelliJ
- Learn IDE-specific features
- Create efficient workflows

## VSCodeVim Setup

### Settings Configuration

```json
{
  "vim.easymotion": true,
  "vim.incsearch": true,
  "vim.useSystemClipboard": true,
  "vim.useCtrlKeys": true,
  "vim.hlsearch": true,
  "vim.insertModeKeyBindings": [
    {
      "before": ["j", "k"],
      "after": ["<Esc>"]
    }
  ],
  "vim.normalModeKeyBindingsNonRecursive": [
    {
      "before": ["<leader>", "f"],
      "commands": ["workbench.action.quickOpen"]
    }
  ]
}
```

## IdeaVim Configuration

### .ideavimrc Setup

```vim
" Basic settings
set scrolloff=5
set incsearch
set hlsearch
set clipboard+=unnamed
set number
set relativenumber

" Plugins
set surround
set multiple-cursors
set commentary
set easymotion

" Key mappings
let mapleader=" "
map <leader>f <Action>(GotoFile)
map <leader>g <Action>(FindInPath)
map <leader>b <Action>(Switcher)
```

## IDE-Specific Features

### VSCode Commands

1. Quick Open (`workbench.action.quickOpen`)
2. Format Document (`editor.action.formatDocument`)
3. Go to Definition (`editor.action.goToDefinition`)
4. Rename Symbol (`editor.action.rename`)

### IntelliJ Actions

1. Go to File (`GotoFile`)
2. Find in Path (`FindInPath`)
3. Rename Element (`RenameElement`)
4. Show Intentions (`ShowIntentionActions`)

## Workflow Integration

### VSCode Workflow

1. Find in files (`<leader>g`)
2. Quick open (`<leader>f`)
3. Toggle sidebar (`<leader>b`)
4. Format document (`<leader>F`)

### IntelliJ Workflow

1. Navigate to class (`<leader>c`)
2. Find usages (`<leader>u`)
3. Quick fix (`<leader>.`)
4. Refactor this (`<leader>r`)

## Command Reference

### VSCode-specific

- `:vscode {command}` - Run VSCode command
- `:call VSCodeNotify()` - Call VSCode API
- `:call VSCodeCall()` - Synchronous API call

### IntelliJ-specific

- `:action {command}` - Run IntelliJ action
- `:map` - List all mappings
- `:set` - Show current settings

## Best Practices

1. Keep configurations in sync
2. Use IDE features when appropriate
3. Maintain Vim muscle memory
4. Leverage IDE-specific tools
5. Regular mapping updates
