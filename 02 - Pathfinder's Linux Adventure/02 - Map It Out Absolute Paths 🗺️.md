# Map It Out: Absolute Paths 🗺️

## What It Is

An **absolute path** is the full address of a file or folder, starting from the root directory (`/`). It’s like giving GPS coordinates—it always points to the same place, no matter where you are in Linux.

- Starts with `/` (e.g., `/home/user/docs/plan.txt`).
- Includes every folder from `/` to the file.

## Why It Matters

Absolute paths are foolproof. Use them when you need to be exact, like running a specific program or accessing a file deep in the system.

## Big Example

You’re organizing festival files and need to work with exact locations.

1. **Create a file with an absolute path**:
    
    ```bash
    echo "Main Stage" > /home/user/festival/stage.txt
    ```
    
    This creates `stage.txt` in `/home/user/festival`.
    
2. **Read it**:
    
    ```bash
    cat /home/user/festival/stage.txt
    ```
    
    Output:
    
    ```
    Main Stage
    ```
    
3. **Run a script**:
    
    ```bash
    echo "echo Planning festival" > /home/user/scripts/plan.sh
    chmod +x /home/user/scripts/plan.sh
    /home/user/scripts/plan.sh
    ```
    
    Output:
    
    ```
    Planning festival
    ```
    
4. **Try from anywhere**:
    
    ```bash
    cd /tmp
    cat /home/user/festival/stage.txt
    ```
    
    Still works because `/home/user/festival/stage.txt` is absolute.
    

## When to Use

- Running programs with exact locations.
- Accessing files when your location might change.
- Sharing paths with others (they’re universal).

## Exercise

**Task**: Work with absolute paths.

1. Create a file `/home/user/festival/bands.txt`:
    
    ```bash
    echo "The Strokes" > /home/user/festival/bands.txt
    ```
    
2. Read it:
    
    ```bash
    cat /home/user/festival/bands.txt
    ```
    
3. Move to `/tmp` and read it again:
    
    ```bash
    cd /tmp
    cat /home/user/festival/bands.txt
    ```
    
4. Create and run a script `/home/user/festival/info.sh`:
    
    ```bash
    echo "echo Festival 2025" > /home/user/festival/info.sh
    chmod +x /home/user/festival/info.sh
    /home/user/festival/info.sh
    ```
    

#absolute-paths

---
