# Connect with Links 🔗

## `ln -s` - Create Symbolic Links

- **What it does**: `ln -s` creates a symbolic link (symlink), which is like a shortcut to another file or folder.
    
- **Why I use it**: It lets me access a file from multiple places without making copies, saving space.
    
- **Example**:
    
    ```bash
    ln -s /home/user/docs/report.pdf ./report.pdf
    ```
    
    Creates a shortcut named `report.pdf` in the current directory, pointing to the original in `/home/user/docs`.
    
- **How it works**: If I open `./report.pdf`, it’s like opening the original `report.pdf`.
    
- **Another example**:
    
    ```bash
    ln -s /home/user/music/favorites.m3u playlist.m3u
    ```
    
    Makes a shortcut to my music playlist.
    
- **When to use**: When I want a file to appear in multiple places without duplicating it. #ln-s
    

## `file` - Check File Type

- **What it does**: `file` tells me what kind of file something is, like a text file, PDF, or symlink.
    
- **Why I use it**: It helps me confirm if a file is what I think it is or if it’s a shortcut.
    
- **Example**:
    
    ```bash
    file report.pdf
    ```
    
    Output: `report.pdf: PDF document`
    
    ```bash
    file ./shortcut.pdf
    ```
    
    Output: `shortcut.pdf: symbolic link to /home/user/docs/report.pdf`
    
- **When to use**: When I’m curious about a file’s type or need to verify a symlink. #file
    

---
