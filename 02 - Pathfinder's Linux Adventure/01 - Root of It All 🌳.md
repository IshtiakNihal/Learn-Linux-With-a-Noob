# Root of It All 🌳

## What It Is

The **root directory** is the topmost folder in Linux, written as `/`. It’s like the main trunk of a tree where all other folders and files branch out. Everything in Linux—every file, folder, or drive—lives somewhere under `/`.

- Think of it as the "Local Disk (C:)" in Windows, but in Linux, it’s just `/`.
- It contains major folders like `/home`, `/etc`, `/tmp`, and more.

## Why It Matters

The root directory is your starting point for understanding where things are. When you use paths, you often reference `/` to be exact about a file’s location.

## Big Example

You’re setting up a music festival and need to store files across Linux.

1. **Check what’s in the root directory**:
    
    ```bash
    ls /
    ```
    
    Output might be:
    
    ```
    bin  dev  etc  home  lib  proc  root  tmp  usr  var
    ```
    
    These are the main branches under `/`.
    
2. **Look inside a root folder**:
    
    ```bash
    ls /home
    ```
    
    Output:
    
    ```
    user
    ```
    
    `/home` has a folder for you, like `/home/user`.
    
3. **Create a festival folder**:
    
    ```bash
    mkdir /tmp/festival
    ```
    
    Placed in `/tmp` (a root-level folder for temporary files).
    
4. **Confirm it’s there**:
    
    ```bash
    ls /tmp
    ```
    
    Output:
    
    ```
    festival
    ```
    

## When to Use

- Accessing system-wide folders (e.g., `/etc` for configs).
- Writing absolute paths starting from `/`.
- Understanding the Linux file system’s structure.

## Exercise

**Task**: Explore the root directory.

1. List the contents of `/`:
    
    ```bash
    ls /
    ```
    
2. Check inside `/home`:
    
    ```bash
    ls /home
    ```
    
3. Create a folder in `/tmp` called `test_fest`:
    
    ```bash
    mkdir /tmp/test_fest
    ```
    
4. Verify it’s there:
    
    ```bash
    ls /tmp
    ```
    
5. Remove it:
    
    ```bash
    rm -r /tmp/test_fest
    ```
    

#root-directory

---
