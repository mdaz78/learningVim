# Day 5: Search, Navigation & Substitute

## Goals:

- Learn to move quickly within files using search
- Get comfortable with precise navigation
- Master substitution to replace text like a boss

## Searching:

- `/pattern`: Search forward for `pattern`
- `?pattern`: Search backward for `pattern`
- `n`: Repeat search in the same direction
- `N`: Repeat search in the opposite direction

## Navigation Shortcuts:

- `G`: Go to the end of the file
- `gg`: Go to the start of the file
- `:10`: Go to line 10
- `H`, `M`, `L`: Move to the top, middle, or bottom of the screen
- `fx`: Jump to the next occurrence of character `x` on the current line
- `Fx`: Jump backward to `x`
- `tx`, `Tx`: Jump until (before) character `x`

## Substitute:

- `:s/old/new/`: Replace `old` with `new` on the current line (first occurrence)
- `:s/old/new/g`: Replace all occurrences on the current line
- `:%s/old/new/g`: Replace all occurrences in the entire file
- `:%s/old/new/gc`: Confirm each replacement

## Exercises:

### 1. Search and Replace:

- Search for a specific word, then replace it using `:s/old/new/`.
- Try using the `g` flag to replace all occurrences on the line.

### 2. Navigation:

- Move to the top, middle, and bottom of the screen using `H`, `M`, `L`.
- Use `/` to search for a word and `n`/`N` to navigate through occurrences.

### 3. Substitute Across the Entire File:

- Replace a word across the entire file using `:%s/old/new/g`.

## Assignment:

1. Open `day5.txt` and practice all search, navigation, and substitution commands.
2. Use `/`, `n`, `N` to search and navigate.
3. Replace text using `:s/old/new/` and `:%s/old/new/g`.
4. Save and commit:
   ```bash
   git add day5.txt
   git commit -m "Day 5: Search, Navigation & Substitute"
   ```
