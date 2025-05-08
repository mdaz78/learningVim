# Day 7 – Marks in Vim

## 🎯 Goal:

Learn to set, navigate, and manage marks in Vim for jumping between important positions in your files.

---

## 📘 What Are Marks?

Marks are bookmarks you can set in your files to quickly jump to specific lines or even exact character positions. Great for navigating large files or jumping between edits.

---

## 🪧 Types of Marks

| Type         | Syntax         | Description                                 |
| ------------ | -------------- | ------------------------------------------- |
| Local marks  | `ma`           | Marks a position in the current file        |
| Jump to mark | `'a`           | Jump to the beginning of the line of mark a |
| Jump (exact) | `` `a ``       | Jump to exact position of mark a            |
| File marks   | `'A`–`'Z`      | Between files (uppercase letters)           |
| Last insert  | `` `. ``       | Last inserted text                          |
| Last jump    | ` ` \`\`       | Last cursor jump                            |
| Last change  | \`\` `[`, `']` | Start/end of last change                    |

---

## 🛠️ Basic Usage

### Set a Mark

```vim
ma     " Set mark 'a' at the current position
```

### Jump to a Mark

```vim
'a     " Jump to line of mark 'a'
`a     " Jump to exact cursor position of mark 'a'
```

### List Marks

```vim
:marks     " Show all current marks
```

### Delete a Mark

```vim
:delmarks a     " Delete mark 'a'
:delmarks A-Z   " Delete all file marks
```

---

## 💪 Exercises

1. Set a mark at the beginning of a function.
2. Move somewhere else, then jump back using `'a` and `` `a ``.
3. Try viewing all your marks with `:marks`.
4. Create an uppercase mark (`'M`) in a different file, then navigate to it.
5. Use `` `. `` to jump to the last insertion point.
6. Use `` `[ `` and `']` to view a recent change.

---

## ✅ Tips

- Combine marks with macros and buffers for a productivity boost.
- Use file marks (`'A`) for jumping across files — great in multi-file projects.
- Backtick (` \``) for exact spot, apostrophe ( `'\`) for line start.

---

## 📈 Coming Up Tomorrow:

**Macros** – Automate repetitive tasks by recording and replaying keystrokes!
