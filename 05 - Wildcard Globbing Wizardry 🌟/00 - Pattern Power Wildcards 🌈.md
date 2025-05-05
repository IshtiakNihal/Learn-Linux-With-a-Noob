# Pattern Power: Wildcards 🌈

Wildcards are special characters I use in the terminal to match filenames or paths. They let me select multiple files without typing every name. The shell (like Bash) expands these patterns into matching files before running my command. Here’s how each one works!

## `*` - Match Any Characters

- **What it does**: The `*` wildcard matches **any characters** (zero or more) in a filename, except for slashes (`/`) or hidden files starting with a dot (`.`).
    
- **Why I use it**: It’s like saying “grab everything” when I want all files that fit a pattern—super flexible!
    
- **Examples**:
    
    - **List all files starting with “note”**:
        
        ```bash
        ls note_*
        ```
        
        If I have `note_1.txt`, `note_2.txt`, `note_final.doc`, output is:
        
        ```
        note_1.txt  note_2.txt  note_final.doc
        ```
        
        `note_*` matches any filename starting with `note_`.
        
    - **List all text files**:
        
        ```bash
        ls *.txt
        ```
        
        Output: `note_1.txt note_2.txt memo.txt`
        
        `*.txt` matches any filename ending with `.txt`.
        
    - **What if nothing matches?**:
        
        ```bash
        ls random_*
        ```
        
        If no files start with `random_`, the shell leaves it as `random_*` (no error, just no matches).
        
    - **Path example**:
        
        ```bash
        ls /home/user/doc*
        ```
        
        Matches directories like `/home/user/documents` or files like `/home/user/doc.txt`.
        
- **When to use**: When I want to work with multiple files that share a pattern, like all `.jpg` images or files with a certain prefix.
    
- **Tip**: `*` skips hidden files (like `.bashrc`) unless I use `.*`, so I don’t accidentally mess with configs! #wildcard-star
    

## `?` - Match One Character

- **What it does**: The `?` wildcard matches **exactly one character** in a filename, except for slashes (`/`) or a leading dot (`.`).
    
- **Why I use it**: It’s perfect when I know a filename’s structure but one character varies—like a single-digit version number.
    
- **Examples**:
    
    - **Match single-character suffixes**:
        
        ```bash
        ls file_?
        ```
        
        If I have `file_a`, `file_b`, `file_cc`, output is:
        
        ```
        file_a  file_b
        ```
        
        `file_?` matches `file_` plus **one** character, so `file_cc` (two characters after `_`) is skipped.
        
    - **Match two-character suffixes**:
        
        ```bash
        ls file_??
        ```
        
        Output: `file_cc`
        
        `file_??` matches `file_` plus **two** characters, so only `file_cc` fits.
        
    - **Specific use**:
        
        ```bash
        ls note_?.txt
        ```
        
        Matches `note_1.txt`, `note_2.txt`, but not `note_10.txt` (because `10` is two characters).
        
- **When to use**: When I need precision, like matching files with a single unknown or variable character.
    
- **Tip**: Each `?` is one character—no more, no less—so I can stack them for exact lengths! #wildcard-question
    

## `[]` - Match One Character from a Set

- **What it does**: Square brackets `[abc]` match **one character** from the set inside, like `a`, `b`, or `c`. It’s pickier than `?`.
    
- **Why I use it**: It lets me choose specific characters I’m interested in, like only certain letters or numbers.
    
- **Examples**:
    
    - **Match specific suffixes**:
        
        ```bash
        ls file_[ab]
        ```
        
        If I have `file_a`, `file_b`, `file_c`, output is:
        
        ```
        file_a  file_b
        ```
        
        `file_[ab]` matches `file_` plus `a` or `b`, so `file_c` is ignored.
        
    - **Match numbers**:
        
        ```bash
        ls note_[12].txt
        ```
        
        Output: `note_1.txt note_2.txt`
        
        `note_[12]` matches `note_` plus `1` or `2`, skipping `note_3.txt`.
        
    - **Path example**:
        
        ```bash
        ls /home/user/doc[12]/*
        ```
        
        Matches files in `/home/user/doc1` or `/home/user/doc2`, but not `/home/user/doc3`.
        
- **When to use**: When I want to limit matches to a small, specific group of characters.
    
- **Tip**: Think of `[abc]` as a menu: “Pick exactly one from these options.” #wildcard-brackets
    

## `[!]` - Match One Character NOT in a Set

- **What it does**: `[!abc]` matches **one character** that is **not** `a`, `b`, or `c`. It’s the opposite of `[abc]`.
    
- **Why I use it**: It’s great for excluding certain characters while still matching one in a specific spot.
    
- **Examples**:
    
    - **Exclude specific suffixes**:
        
        ```bash
        ls file_[!ab]
        ```
        
        If I have `file_a`, `file_b`, `file_c`, output is:
        
        ```
        file_c
        ```
        
        `file_[!ab]` matches `file_` plus any single character that’s not `a` or `b`, so only `file_c` fits.
        
    - **Combine with** `*`:
        
        ```bash
        ls [!n]*
        ```
        
        If I have `note.txt`, `memo.txt`, `new.txt`, output is:
        
        ```
        memo.txt  new.txt
        ```
        
        `[!n]*` matches filenames where the first character isn’t `n`, so `note.txt` (starts with `n`) is skipped.
        
    - **Why** `[!pwn]` **vs** `[!pwn]*` **confused me**:
        
        - `[!pwn]` alone:
            
            ```bash
            ls [!pwn]
            ```
            
            Matches **one-character** filenames that aren’t `p`, `w`, or `n`. If I have `a`, `p`, `z`, output is:
            
            ```
            a  z
            ```
            
            Only single characters not in `pwn` match.
            
        - `[!pwn]*`:
            
            ```bash
            ls [!pwn]*
            ```
            
            Matches **any filename** where the first character isn’t `p`, `w`, or `n`. If I have `apple.txt`, `pear.txt`, `water.txt`, output is:
            
            ```
            apple.txt  pear.txt
            ```
            
            `water.txt` is skipped because it starts with `w`.
            
- **When to use**: When I want to exclude specific characters in a position, like avoiding certain prefixes.
    
- **Tip**: `[!abc]` is like saying, “Anything but these guys!” Add `*` to catch longer names. #wildcard-not-brackets
    

---

