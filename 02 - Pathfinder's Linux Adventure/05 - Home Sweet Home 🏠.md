# Home Sweet Home 🏠

## What It Is

The **home directory** is your personal folder, usually `/home/user` (or `/home/hacker` in some setups). It’s where your files, like documents and settings, live.

- Shortcut: `~` expands to `/home/user`.
- Example: `~/docs` means `/home/user/docs`.

## Why It Matters

It’s your safe space for files and a quick way to navigate with `~`. You often start here for personal projects.

## Big Example

You’re storing festival plans in your home directory.

1. **Go home**:
    
    ```bash
    cd ~
    pwd
    ```
    
    Output:
    
    ```
    /home/user
    ```
    
2. **Create a file**:
    
    ```bash
    echo "Budget" > ~/festival/budget.txt
    ```
    
3. **Read it**:
    
    ```bash
    cat ~/festival/budget.txt
    ```
    
    Output:
    
    ```
    Budget
    ```
    
4. **From anywhere**:
    
    ```bash
    cd /tmp
    cat ~/festival/budget.txt
    ```
    
    Still works because `~` is absolute.
    

## When to Use

- Storing personal files.
- Using `~` for quick paths.
- Returning to a familiar spot.

## Exercise

**Task**: Use the home directory.

1. Go to `~`:
    
    ```bash
    cd ~
    ```
    
2. Create a file:
    
    ```bash
    echo "Plan" > ~/festival/plan.txt
    ```
    
3. Read it:
    
    ```bash
    cat ~/festival/plan.txt
    ```
    
4. Move to `/etc` and read again:
    
    ```bash
    cd /etc
    cat ~/festival/plan.txt
    ```
    
5. Create another file with `~`:
    
    ```bash
    echo "Notes" > ~/festival/notes.txt
    ```
    

#home-directory

---
