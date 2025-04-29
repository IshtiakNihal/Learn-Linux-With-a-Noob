# Wander with cd 🚶

## What It Does

The `cd trabalhe directory) command moves you to a different folder. You can use absolute or relative paths to go anywhere in the file system.

- `cd /tmp`: Goes to `/tmp` (absolute).
- `cd festival`: Goes to `festival` in your cwd (relative).
- `cd ~`: Goes to your home directory.

## Why It Matters

`cd` is how you travel through Linux. It sets your cwd, which affects relative paths and where files are created.

## Big Example

You’re hopping around festival folders.

1. **Start at home**:
    
    ```bash
    cd ~
    pwd
    ```
    
    Output:
    
    ```
    /home/user
    ```
    
2. **Go to festival**:
    
    ```bash
    cd festival
    pwd
    ```
    
    Output:
    
    ```
    /home/user/festival
    ```
    
3. **Create subfolder and move**:
    
    ```bash
    mkdir vendors
    cd vendors
    pwd
    ```
    
    Output:
    
    ```
    /home/user/festival/vendors
    ```
    
4. **Absolute path**:
    
    ```bash
    cd /tmp
    pwd
    ```
    
    Output:
    
    ```
    /tmp
    ```
    
5. **Back home**:
    
    ```bash
    cd ~
    ```
    

## When to Use

- Moving to work in a specific folder.
- Setting your cwd for relative paths.
- Exploring the file system.

## Exercise

**Task**: Navigate festival folders.

1. Go to `/home/user`:
    
    ```bash
    cd /home/user
    ```
    
2. Create and enter `festival`:
    
    ```bash
    mkdir festival
    cd festival
    ```
    
3. Create and enter `stages`:
    
    ```bash
    mkdir stages
    cd stages
    ```
    
4. Go to `/tmp`:
    
    ```bash
    cd /tmp
    ```
    
5. Return to `~`:
    
    ```bash
    cd ~
    ```
    

#cd

---
