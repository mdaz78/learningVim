# Day 23: Advanced Search Techniques

## Goals:

- Master Vim's advanced search capabilities
- Learn to use vimgrep effectively
- Navigate search results using quickfix
- Master complex search patterns

## Vimgrep Search

### Basic Usage

```vim
:vimgrep /pattern/ **/*.js    " Search in all JS files
:vimgrep /function/ **/*.js   " Find all functions
```

### Example Files

```javascript
// File1.js
function getData() {
  return fetch('/api/data');
}

// File2.js
async function fetchData() {
  const data = await getData();
  return data;
}

// File3.js
function processData(data) {
  return data.map((item) => item.id);
}
```

## Quickfix Navigation

### Commands

- `:cn` - Next match
- `:cp` - Previous match
- `:cc` - Current match
- `:copen` - Open quickfix window
- `:cclose` - Close quickfix window

### Workflow

1. Search with vimgrep
2. Navigate results with quickfix
3. Make changes as needed
4. Move to next match

## Advanced Patterns

### Pattern Types

1. Camel case: `myVariableName`
2. Snake case: `my_variable_name`
3. Email: `user@example.com`
4. URL: `https://example.com`
5. IP: `192.168.1.1`
6. Date: `2023-05-13`

### Search Modifiers

- `\v` - Very magic (simplified regex)
- `\c` - Case insensitive
- `\<` `\>` - Word boundaries

## Search and Replace Examples

### Parameter Swapping

```vim
:%s/function(\([^,]*\), \([^)]*\))/function(\2, \1)/g
```

### Date Format Conversion

```vim
:%s/\v(\d{4})\/(\d{2})\/(\d{2})/\3-\2-\1/g
```

### Style Convention Change

```vim
:%s/\v([a-z])-([a-z])/\1\u\2/g
```

## Best Practices

1. **Search Organization**

   - Use specific patterns
   - Leverage file type filters
   - Structure complex searches

2. **Navigation Efficiency**

   - Use quickfix window
   - Jump between matches
   - Save search patterns

3. **Pattern Building**

   - Start simple
   - Test incrementally
   - Use magic mode appropriately

4. **Result Management**
   - Filter results
   - Save result lists
   - Document complex patterns

## Quick Reference

- `:vimgrep` - Search in files
- `:grep` - External grep
- `:lgrep` - Location list grep
- `:Rg` - Ripgrep (if installed)
- `:cw` - Open quickfix
- `:lw` - Open location list
