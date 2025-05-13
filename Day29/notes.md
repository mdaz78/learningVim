# Day 29: Full Project Workflow

## Goals:

- Master complete project workflow in Vim
- Learn efficient project navigation
- Practice Git operations
- Integrate testing and debugging

## Project Setup

### Directory Structure

```bash
my-project/
├── src/
│   ├── index.ts
│   ├── utils/
│   └── components/
└── tests/
    └── index.test.ts
```

## Navigation Commands

### File Navigation

- `<leader>ff` - Find files
- `<leader>fg` - Live grep (search in files)
- `<leader>fb` - Browse buffers
- `<leader>fh` - Search help tags

### Project Movement

1. Quick file switching
2. Buffer navigation
3. Split management
4. Project-wide search

## Git Operations

### Common Git Commands

- `<leader>gs` - Git status (fugitive)
- `<leader>gd` - Git diff
- `<leader>gc` - Git commit
- `<leader>gp` - Git push
- `<leader>gl` - Git pull

### Workflow Steps

1. Stage changes
2. Review diff
3. Commit changes
4. Push/pull

## Testing & Debug Cycle

### Testing Workflow

1. Write code
2. Run tests (`:term npm test`)
3. Debug with DAP
4. Fix issues
5. Commit changes

### Best Practices

- Keep terminal split open for tests
- Use quickfix for errors
- Leverage LSP for diagnostics

## Exercises

1. **Project Navigation**

   - Practice file finding
   - Use live grep for searching
   - Switch between buffers

2. **Development Flow**

   - Edit multiple files
   - Run tests
   - Debug issues
   - Make fixes

3. **Git Operations**

   - Stage files
   - View diffs
   - Create commits
   - Push changes

4. **Terminal Usage**
   - Run commands
   - View test output
   - Monitor processes
