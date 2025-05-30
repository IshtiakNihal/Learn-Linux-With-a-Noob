# Nearby Trails: Relative Paths 📍

## What It Is

A **relative path** describes a file or folder’s location based on where you are right now—your **current working directory (cwd)**. It doesn’t start with `/`, so it’s shorter but depends on your position.

- Example: If you’re in `/home/user`, the relative path to `/home/user/festival/plan.txt` is just `festival/plan.txt`.

## Why It Matters

Relative paths are quick and convenient when you’re already close to the file. They save typing, especially in your own folders.

## Big Example

You’re working in `/home/user/festival`.

1. **Set up folders**:
    
    ```bash
    mkdir /home/user/festival
    cd /home/user/festival
    ```
    
2. **Create files**:
    
    ```bash
    echo "Rock" > genres.txt
    mkdir plans
    echo "Saturday" > plans/day1.txt
    ```
    
3. **Use relative paths**:
    
    ```bash
    cat genres.txt
    ```
    
    Output:
    
    ```
    Rock
    ```
    
    ```bash
    cat plans/day1.txt
    ```
    
    Output:
    
    ```
    Saturday
    ```
    
4. **Move around**:
    
    ```bash
    cd plans
    cat day1.txt
    ```
    
    Works because `day1.txt` is in your cwd.
    
5. **Wrong cwd**:
    
    ```bash
    cd /tmp
    cat genres.txt
    ```
    
    Fails unless `genres.txt` exists in `/tmp`.
    

## When to Use

- Working in your current folder or nearby.
- Writing quick commands.
- Scripts where you know the starting point.

## Exercise

**Task**: Use relative paths.

1. Go to `/home/user`:
    
    ```bash
    cd /home/user
    ```
    
2. Create a folder and file:
    
    ```bash
    mkdir events
    echo "Concert" > events/music.txt
    ```
    
3. Read with relative path:
    
    ```bash
    cat events/music.txt
    ```
    
4. Move inside `events` and read:
    
    ```bash
    cd events
    cat music.txt
    ```
    
5. Try from `/tmp` (should fail):
    
    ```bash
    cd /tmp
    cat events/music.txt
    ```
    

#relative-paths

---
