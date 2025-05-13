# Day 22: Code Folding Practice

## Goals:

- Master Vim's folding mechanisms
- Learn different folding methods
- Navigate and manage folds efficiently
- Use folds for code organization

## Manual Folding

### Basic Commands

- `zf` - Create fold (in visual mode)
- `zd` - Delete fold
- `zE` - Eliminate all folds

### Example Structure

```
Section 1 {
    Subsection 1.1 {
        Content here
        More content
        Even more
    }

    Subsection 1.2 {
        Another block
        Of content
        To practice with
    }
}
```

## Fold Navigation

### Commands

- `zc` - Close fold
- `zo` - Open fold
- `za` - Toggle fold
- `zR` - Open all folds
- `zM` - Close all folds

### Nested Example

```
Class Example {
    Method 1 {
        Line 1
        Line 2
        Line 3
    }

    Method 2 {
        Line 1
        Line 2
        Line 3
    }
}
```

## Fold Methods

### Available Methods

1. `manual` - Created by commands
2. `indent` - Based on indentation
3. `syntax` - Based on language syntax
4. `marker` - Based on special markers

### Setting Fold Method

```vim
:set foldmethod=indent  " Use indent method
:set foldmethod=syntax  " Use syntax method
:set foldmethod=marker  " Use marker method
```

## Marker Folding

### Marker Format

```vim
" {{{1 marks start of level 1 fold
" }}}1 marks end of level 1 fold
```

### Example

```
Section A {{{1
    Content A
    More A
}}}1

Section B {{{1
    Content B
    More B
}}}1
```

## Best Practices

1. **Choose Appropriate Method**

   - Manual for temporary folds
   - Indent for Python-like code
   - Syntax for structured languages
   - Marker for persistent folds

2. **Navigation Tips**

   - Use `zj`/`zk` to move between folds
   - `zm`/`zr` to fold/unfold incrementally
   - Save fold state in views

3. **Organization**

   - Fold long functions
   - Group related code
   - Keep documentation visible

4. **Performance**
   - Don't over-fold
   - Use appropriate fold method
   - Clean up unused folds

## Quick Reference

### Creation

- `zf` - Create fold
- `zd` - Delete fold
- `zE` - Eliminate all folds

### Navigation

- `zj` - Next fold
- `zk` - Previous fold
- `[z` - Start of current fold
- `]z` - End of current fold

### Opening/Closing

- `zo` - Open fold
- `zc` - Close fold
- `za` - Toggle fold
- `zR` - Open all
- `zM` - Close all
