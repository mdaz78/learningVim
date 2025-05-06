# Day 4: Yank, Paste, and Change

## Goals:

- Learn to copy (yank) text
- Use different ways to paste
- Master change commands (like replace and modify)

## Yank (Copy) Commands:

- `yy`: Yank the current line
- `yw`: Yank a word
- `y$`: Yank from the cursor to the end of the line
- `y0`: Yank from the cursor to the start of the line
- `v` + movement + `y`: Visual-select and yank

## Paste Commands:

- `p`: Paste after the cursor or line
- `P`: Paste before the cursor or line

## Change Commands:

- `cw`: Change word
- `c$`: Change to the end of the line
- `cc`: Change the whole line
- `C`: Same as `c$`
- `s`: Substitute one character
- `S`: Substitute the entire line

## Exercises:

### 1. Yank and Paste Lines

- `yy`, move, then `p` or `P`

### 2. Yank and Paste Words

- `yw`, move, then `p` or `P`

### 3. Yank to End/Start of Line

- `y$`, `y0`, then paste

### 4. Visual Mode Yank

- `v` + movement, then `y` and `p`

### 5. Change Word

- Use `cw`, type new word, then `Esc`

### 6. Change to End of Line

- `c$`, type new content, then `Esc`

### 7. Change Entire Line

- `cc`, type new content, then `Esc`

### 8. Substitute Character

- Use `s` to replace a single character
- Use `S` to replace the entire line

## Assignment:

1. Open `day4.txt` and perform each exercise.
2. Practice using yank, paste, and change commands.
3. Save and commit:
   ```bash
   git add day4.txt
   git commit -m "Day 4: Yank, Paste, Change"
   ```
