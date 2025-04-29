# Where Am I? Current Directory 📍

## What It Is

The **current working directory (cwd)** is the folder you’re currently in while using the terminal. It’s like your current spot on a map, and relative paths depend on it.

- Check it with `pwd` (print working directory).

## Why It Matters

Knowing your cwd helps you use relative paths correctly and understand where commands will look for files.

## Big Example

You’re navigating festival folders.

1. **Check your cwd**:
    
    ```bash
    pwd
    ```
    
    Output:
    
    ```
    /home/user
    ```
    
2. **Move and check**:
    
    ```bash
    cd festival
    pwd
    ```
    
    Output:
    
    ```
    /home/user/festival
    ```
    
3. **Create a file**:
    
    ```bash
    echo "Lights" > setup.txt
    cat setup.txt
    ```
    
    Works because `setup.txt` is in your cwd.
    
4. **Relative path depends on cwd**:
    
    ```bash
    cd plans
    cat setup.txt
    ```
    
    Fails unless `setup.txt` is in `plans`.
    

## When to Use

- Before using relative paths.
- To confirm your location.
- Debugging path errors.

## Exercise

**Task**: Track your cwd.

1. Check cwd:
    
    ```bash
    pwd
    ```
    
2. Move to `/tmp`:
    
    ```bash
    cd /tmp
    pwd
    ```
    
3. Create a file:
    
    ```bash
    echo "Temp" > note.txt
    ```
    
4. Move to `/home/user` and try reading:
    
    ```bash
    cd /home/user
    cat note.txt
    ```
    
    Should fail.
    
5. Go back and read:
    
    ```bash
    cd /tmp
    cat note.txt
    ```
    

#cwd

---
