# 🧠 Vim 30-Day Cheatsheet

## Week 1 – The Essentials

### Day 1: Modes & Movement

- `i`, `a`, `I`, `A`, `o`, `O`: Insert modes
- `h`, `j`, `k`, `l`: Move left, down, up, right
- `w`, `b`, `e`: Word movements
- `0`, `^`, `$`: Line movements
- `gg`, `G`: File start/end

### Day 2: Visual Mode

- `v`: Character-wise visual mode
- `V`: Line-wise visual mode
- `Ctrl+v`: Block visual mode
- `d`, `y`, `p`: Delete, yank, paste in visual mode

### Day 3: Delete & Undo

- `x`, `X`: Delete char under/before cursor
- `dd`: Delete line
- `dw`, `d$`, `d0`: Delete word, to end/start of line
- `u`: Undo, `Ctrl+r`: Redo

### Day 4: Yank, Paste, Change

- `yy`, `yw`, `y$`, `y0`: Yank
- `p`, `P`: Paste
- `cw`, `cc`, `c$`, `C`: Change
- `s`, `S`: Substitute char/line

### Day 5: Search, Navigation, Substitute

- `/pattern`, `?pattern`: Search
- `n`, `N`: Repeat search
- `:s/old/new/`, `:%s/old/new/gc`: Replace text
- `fx`, `tx`, `H`, `M`, `L`, `:10`: Navigate

---

## Week 2 – Power Editing

### Day 6: Registers

- `"ayw`: Yank word to register `a`
- `"ap`: Paste from register `a`
- `:reg`: Show registers

### Day 7: Marks

- `ma`: Set mark `a`
- `'a`, `` `a ``: Jump to mark line/char

### Day 8: Macros

- `q[a-z]`: Start recording
- `@a`: Play macro in register `a`
- `@@`: Repeat last macro

### Day 9: Search in Files

- `:vimgrep /pattern/ **/*.ts`
- `:copen`, `:cnext`, `:cprev`

### Day 10: Buffers, Tabs & Windows

- `:e file`, `:bnext`, `:bprev`, `:bd`
- `:tabnew`, `gt`, `gT`
- `:split`, `:vsplit`, `Ctrl+w w`

### Day 11: Formatting

- `gg=G`: Auto indent entire file
- `=`, `>>`, `<<`: Indentation

### Day 12: Spelling & Help

- `:set spell`, `]s`, `[s`, `z=`
- `:help`, `:help <command>`

---

## Week 3 – Intermediate Mastery

### Day 13: File Navigation

- `:Ex`, `:Sex`, `:Vex`: File explorers
- `gf`: Go to file under cursor

### Day 14: Tags & Ctags

- `:tag`, `:tags`, `:tnext`
- `Ctrl-]`, `Ctrl-t`

### Day 15: Vimrc & Settings

- `~/.vimrc`, `:source %`
- Customize keymaps, settings

### Day 16: Plugin Managers

- vim-plug, packer.nvim basics
- `PlugInstall`, `PlugUpdate`

### Day 17: Autocommands

- `:autocmd BufWritePre *.js :%s/console.log//g`

### Day 18: Abbreviations & Mappings

- `:iabbrev`, `:nmap`, `:imap`
- Remap `jk` to `<Esc>`, etc.

### Day 19: Terminal Mode

- `:terminal`
- `Ctrl-w N`: Normal mode in terminal

---

## Week 4 – Advanced & Workflow

### Day 20: Folding

- `zf`, `zo`, `zc`, `zd`, `zR`, `zM`

### Day 21: Text Objects

- `ciw`, `diw`, `yiw`
- `ci"`, `di]`, `va{`, `vi(`

### Day 22: Advanced Search

- `:g/pattern/`, `:v/pattern/`

### Day 23: Grep + sed + awk in Vim

- `:!grep TODO %`, `:!awk '{print $1}' %`

### Day 24: Scratch Buffers

- `:new`, `:enew`, `:noswapfile`

### Day 25: Sessions

- `:mksession`, `:source session.vim`

### Day 26: Git in Vim

- Fugitive basics: `:Gstatus`, `:Gdiff`, `:Gcommit`

---

## Final Stretch – Polish & Projects

### Day 27: Snippets

- UltiSnips/Luasnip usage
- Expand, jump, create

### Day 28: LSP Integration

- Use coc.nvim or nvim-lsp
- Go-to-definition, diagnostics

### Day 29: Tmux + Vim

- Split workflows, send-to-pane
- Use `Ctrl-b` prefix with tmux

### Day 30: Building a Workflow

- Customize .vimrc, keymaps
- Combine macros, search, folds, etc.
