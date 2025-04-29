# Peek at Files 👀

## `cat` - Display File Contents

- **What it does**: The `cat` command (short for "concatenate") prints the entire content of a file to the terminal.
    
- **Why I use it**: It’s great for quickly checking small files, like a to-do list or a short config file.
    
- **Example**:
    
    ```bash
    cat shopping_list.txt
    ```
    
    If `shopping_list.txt` contains:
    
    ```
    Milk
    Bread
    Eggs
    ```
    
    The terminal shows exactly that.
    
- **When to use**: Best for small files, as large files can flood the terminal. #cat
    

## `grep` - Search Inside Files

- **What it does**: `grep` searches for specific words or phrases in a file and shows only the matching lines.
    
- **Why I use it**: When a file is too big for `cat`, `grep` helps me find exactly what I need without scrolling through everything.
    
- **Example**:
    
    ```bash
    grep "Milk" shopping_list.txt
    ```
    
    Output: `Milk` (only the line with “Milk” shows up).
    
- **Another example**:
    
    ```bash
    grep "error" log.txt
    ```
    
    Finds all lines in `log.txt` with the word “error”.
    
- **When to use**: Ideal for logs, configs, or any file where I need to pinpoint specific content. #grep
    

---
