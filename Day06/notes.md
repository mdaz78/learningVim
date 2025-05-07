# Day 6 – Registers in Vim

## 🎯 Goal:

Understand and master Vim registers — what they are, how to use them, and how they empower copy/paste workflows beyond system clipboards.

---

## 📘 What Are Registers?

Registers are like clipboards. Vim has many, each with a name. You can explicitly yank, delete, and paste from a specific register.

---

## 📂 Types of Registers

| Name       | Register Key  | Description                              |
| ---------- | ------------- | ---------------------------------------- |
| Unnamed    | `"` (default) | Most recent yanked/deleted text          |
| Named      | `"a` to `"z`  | 26 user-defined registers                |
| Read-only  | `":`, `".`    | Command history, last inserted text, etc |
| Black Hole | `"_`          | Discards the text                        |
| System     | `"+`, `"*`    | System clipboard (if supported)          |

---

## 🛠️ Basic Usage Examples

### Yank into a Register

```vim
"ayw     " Yank a word into register a
"bY      " Yank a line into register b
```

### Paste from a Register

```vim
"ap      " Paste from register a
"+p      " Paste from system clipboard
```

### Delete into Register

```vim
"adw     " Delete a word and store in register a
```

### Append to Register

```vim
"Ayy     " Append line to register a (uppercase A)
```

### View Registers

```vim
:reg     " Show contents of all registers
```

---

## 💪 Exercises

1. Yank the word `hello` into register `a`.
2. Yank a full line into register `b`, then paste it below.
3. Delete a word into register `c`.
4. Use the black hole register to delete a word without saving it.
5. Append two lines into register `z` using `"Zyy` twice.
6. View all register contents using `:reg`.

---

## ✅ Tips

- You can combine registers with macros: store a macro in a register and replay it.
- Use registers to avoid overwriting clipboard during delete.
- System clipboard (`+`) may need `+clipboard` support in your Vim build.

---

## 📈 Coming Up Tomorrow:

**Marks** – Learn how to jump between important places in files quickly and efficiently!
