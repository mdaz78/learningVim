# Day 25: Debugging with DAP (Debug Adapter Protocol)

## Goals:

- Learn DAP integration in Neovim
- Set up debugging workflows
- Master debugging commands
- Use debugging UI effectively

## Basic Debug Setup

### Sample JavaScript Code

```javascript
function calculateTotal(items) {
  let total = 0;
  for (const item of items) {
    total += item.price;
  }
  return total;
}

const cart = [
  { id: 1, price: 10 },
  { id: 2, price: 20 },
  { id: 3, price: 30 },
];

console.log(calculateTotal(cart));
```

### Debug Commands

- `<leader>db` - Toggle breakpoint
- `<leader>dc` - Continue
- `<leader>dso` - Step over
- `<leader>dsi` - Step into
- `<leader>dK` - Evaluate under cursor

## Debug UI Elements

### Windows

1. Breakpoints window
2. Variables window
3. Watch window
4. Call stack
5. REPL

### Watch Expressions

- `cart.length`
- `total`
- `item.price`

## Conditional Breakpoints

### Types

1. Break when total > 50
2. Break when item.id === 2
3. Break on exception throw

### Configuration

```javascript
// Condition example
total > 50;

// Hit count example
item.id === 2;

// Log point example
console.log('Processing item:', item);
```

## Launch Configurations

### launch.json Example

```json
{
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Debug Current File",
      "program": "${file}"
    }
  ]
}
```

## Advanced Features

### 1. Variable Inspection

- View current values
- Modify values
- Add to watch

### 2. Call Stack Navigation

- View stack frames
- Navigate frames
- Examine scope

### 3. Breakpoint Management

- Enable/disable
- Add conditions
- Set hit counts

### 4. REPL Usage

- Evaluate expressions
- Run commands
- Inspect state

## Best Practices

1. **Breakpoint Strategy**

   - Set strategic points
   - Use conditions wisely
   - Clean up after debugging

2. **Watch Expressions**

   - Monitor key variables
   - Use complex expressions
   - Update as needed

3. **UI Organization**

   - Arrange windows logically
   - Keep relevant info visible
   - Use split layouts effectively

4. **Workflow Integration**
   - Combine with tests
   - Use with LSP
   - Integrate with git
