# Launch Local with ./ 💻

## What It Does

The `./` prefix runs an executable file (like a script or program) in your **current directory**. Linux doesn’t automatically look in your cwd for commands, so `./` tells it, “Run this file right here.”

- Example: `./myscript.sh` runs `myscript.sh` in your cwd.

## Why It Matters

You need `./` to run your own scripts or programs without moving them to a system folder like `/usr/bin`.

## Big Example

You’re running festival scripts.

1. **Create a script**:
    
    ```bash
    echo "echo Welcome to the festival" > /home/user/festival/greet.sh
    chmod +x /home/user/festival/greet.sh
    ```
    
2. **Go to folder**:
    
    ```bash
    cd /home/user/festival
    ```
    
3. **Run it**:
    
    ```bash
    ./greet.sh
    ```
    
    Output:
    
    ```
    Welcome to the festival
    ```
    
4. **Without** `./`:
    
    ```bash
    greet.sh
    ```
    
    Fails with:
    
    ```
    bash: greet.sh: command not found
    ```
    
5. **From another folder**:
    
    ```bash
    cd /tmp
    ./greet.sh
    ```
    
    Fails unless `greet.sh` is in `/tmp`. Use absolute path instead:
    
    ```bash
    /home/user/festival/greet.sh
    ```
    

## When to Use

- Running scripts or programs in your cwd.
- Testing your own code.
- Avoiding path issues with local files.

## Exercise

**Task**: Run festival scripts.

1. Create a script:
    
    ```bash
    echo "echo Music starts now" > /home/user/festival/start.sh
    chmod +x /home/user/festival/start.sh
    ```
    
2. Go to folder and run:
    
    ```bash
    cd /home/user/festival
    ./start.sh
    ```
    
3. Try without `./`:
    
    ```bash
    start.sh
    ```
    
    Note the error.
    
4. Run from `/tmp` with absolute path:
    
    ```bash
    cd /tmp
    /home/user/festival/start.sh
    ```
    
5. Try `./start.sh` in `/tmp` (should fail).
    

#run-commands

---
