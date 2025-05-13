# Day 30: Review and Final Challenge

## Goals:

- Test and reinforce Vim mastery
- Practice complex workflows
- Configure custom dashboard
- Complete speed challenges

## Speed Tests

### Text Manipulation

1. Quick deletions

   - `3dw` - Delete 3 words
   - `ci(` - Change inside parentheses
   - `yap` - Yank a paragraph

2. Search and Replace
   - Find next occurrence
   - Global substitution
   - With confirmation

### Navigation

1. Jump commands
   - `42G` - Go to line 42
   - `/function` - Find next function
   - `%` - Match brackets
   - `]]`, `[[` - Jump between functions

## Custom Dashboard Configuration

### Dashboard Setup

```lua
require('dashboard').setup {
    theme = 'doom',
    config = {
        header = {
            "Welcome to Neovim",
            "Mastered in 30 Days"
        },
        center = {
            {
                icon = ' ',
                desc = 'Find File           ',
                key = 'f',
                action = 'Telescope find_files'
            },
            {
                icon = ' ',
                desc = 'Recent Files        ',
                key = 'r',
                action = 'Telescope oldfiles'
            }
        }
    }
}
```

## Workflow Challenge

### 2-Minute Project Task

1. Open project
2. Find `utils.ts`
3. Extract function
4. Run tests
5. Stage and commit

## Vim Golf Challenges

### Text Transformations

1. Convert case:

   ```
   hello_world -> HelloWorld
   ```

2. Add try/catch:

   ```
   someFunction();
   ```

   to:

   ```
   try {
       someFunction();
   } catch (error) {
       // handle error
   }
   ```

3. Sort lines:
   ```
   banana
   apple
   cherry
   ```

## Key Learnings Review

### Core Skills Mastered

- Efficient navigation
- Text manipulation
- Plugin integration
- Git workflow
- LSP features
- Terminal usage
- Custom configurations

### Best Practices

- Use registers effectively
- Leverage macros for repetition
- Master text objects
- Keep fingers on home row
- Use built-in Vim features

## Next Steps

1. Continue practicing daily
2. Customize your config
3. Learn new plugins
4. Contribute to Vim community
5. Share knowledge with others
