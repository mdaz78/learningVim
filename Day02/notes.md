# Day 2: Insert Mode, Delete, Undo/Redo

## Goals:

- Master Insert Mode: Learn how to enter and exit Insert Mode quickly.
- Learn how to delete text: Use basic deletion commands.
- Learn how to undo and redo changes.

## Key Concepts:

### 1. Insert Mode:

- **Enter Insert Mode**: Press `i` (before the cursor), `I` (beginning of the line), `a` (after the cursor), or `A` (end of the line).
- **Exit Insert Mode**: Press `Esc` to return to Normal Mode.

### 2. Deleting Text:

- `x`: Delete the character under the cursor.
- `dd`: Delete the entire line where the cursor is.
- `D`: Delete from the cursor to the end of the line.
- `dw`: Delete the word from the cursor onward.
- `d$`: Delete from the cursor to the end of the line.

### 3. Undo and Redo:

- `u`: Undo the last change.
- `Ctrl + r`: Redo the undone change.

## Exercise:

1. Open a file (or create a new one if necessary) and practice entering Insert Mode with `i`, `I`, `a`, and `A`. Type some text.
2. Practice exiting Insert Mode by pressing `Esc`.
3. Use the deletion commands (`x`, `dd`, `D`, `dw`, `d$`) to delete parts of your text.
4. Undo and redo changes using `u` and `Ctrl + r`.

## Assignment for Day 2:

1. Open `day2.txt` and write some lines of text.
2. Practice the delete, undo, and redo commands on your file.
3. Commit your changes with the message `"Day 2: Insert Mode, Delete, Undo/Redo"`.
