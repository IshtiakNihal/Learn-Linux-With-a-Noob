# Hunt Down Files 🔍

## `find` - Search for Files

- **What it does**: `find` searches for files or folders based on their name or other criteria.
    
- **Why I use it**: It’s like a superpower for locating files when I forget where I put them.
    
- **Examples**:
    
    - Search the current directory:
        
        ```bash
        find .
        ```
        
        Output: Lists everything, like:
        
        ```
        .
        ./documents
        ./documents/readme.md
        ./photos
        ```
        
    - Search by name:
        
        ```bash
        find . -name "readme.md"
        ```
        
        Output: `./documents/readme.md`
        
    - Search the entire system:
        
        ```bash
        sudo find / -name "config"
        ```
        
        Searches all directories for a file or folder named “config” (needs `sudo` for restricted areas).
        
- **When to use**: When I need to track down a file or see what’s in a directory tree. #find
    

---
