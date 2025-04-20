# Step Up, Step Here: . and .. 🔙

## What They Are

- `.`: The current directory you’re in. It’s like saying, “Right here.”
- `..`: The parent directory (one folder up). It’s like stepping back to the folder containing your cwd.

## Why It Matters

`.` and `..` make navigation and paths flexible. Use them in relative paths to move up or reference your current spot.

## Big Example

You’re working in a festival folder structure.

1. **Set up**:
    
    ```bash
    mkdir -p /home/user/festival/stages/main
    cd /home/user/festival/stages/main
    echo "Headliner" > band.txt
    ```
    
2. **Use** `.`:
    
    ```bash
    cat ./band.txt
    ```
    
    Output:
    
    ```
    Headliner
    ```
    
    `./band.txt` is the same as `band.txt`.
    
3. **Use** `..`:
    
    ```bash
    ls ..
    ```
    
    Output:
    
    ```
    main
    ```
    
    `..` takes you to `/home/user/festival/stages`.
    
4. **Go up and back**:
    
    ```bash
    cd ..
    pwd
    ```
    
    Output:
    
    ```
    /home/user/festival/stages
    ```
    
    ```bash
    cat main/band.txt
    ```
    
    Output:
    
    ```
    Headliner
    ```
    
5. **Multiple** `..`:
    
    ```bash
    cd /home/user/festival/stages/main
    ls ../../..
    ```
    
    Output:
    
    ```
    user
    ```
    
    `../../..` goes up to `/home`.
    

## When to Use

- `.`: Running files in your cwd (e.g., `./script.sh`) or explicit paths.
- `..`: Moving up to parent folders or accessing files above your cwd.
- Building relative paths.

## Exercise

**Task**: Navigate with `.` and `..`.

1. Create a deep folder:
    
    ```bash
    mkdir -p /home/user/festival/stages/vip
    cd /home/user/festival/stages/vip
    ```
    
2. Create a file:
    
    ```bash
    echo "VIP Pass" > ./pass.txt
    ```
    
3. Read it with `.`:
    
    ```bash
    cat ./pass.txt
    ```
    
4. Go up one folder:
    
    ```bash
    cd ..
    pwd
    ```
    
5. Read the file using `..`:
    
    ```bash
    cat vip/pass.txt
    ```
    
    Check with `cat ../../festival/stages/vip/pass.txt` from `/home/user`.
    

#dot-double-dot

---

_Last updated: April 16, 2025_