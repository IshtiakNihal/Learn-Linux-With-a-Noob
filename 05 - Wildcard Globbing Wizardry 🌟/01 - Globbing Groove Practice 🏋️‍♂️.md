# Globbing Groove: Practice 🏋️‍♂️

This section is a festival-themed terminal session to make wildcards second nature through hands-on practice.

## Practice Tasks

1. Create some test files:
    
    ```bash
    touch note_a.txt note_b.txt note_cc.txt note_1.txt note_2.txt
    ```
    
2. Match all notes:
    
    ```bash
    ls note_*
    ```
    
    Should see: `note_1.txt note_2.txt note_a.txt note_b.txt note_cc.txt`
    
3. Match single-character suffixes:
    
    ```bash
    ls note_?
    ```
    
    Should see: `note_1.txt note_2.txt note_a.txt note_b.txt`
    
4. Match specific suffixes:
    
    ```bash
    ls note_[ab].txt
    ```
    
    Should see: `note_a.txt note_b.txt`
    
5. Exclude specific suffixes:
    
    ```bash
    ls note_[!ab].txt
    ```
    
    Should see: `note_1.txt note_2.txt`
    
6. Match all non-numeric prefixes:
    
    ```bash
    ls [!12]*
    ```
    
    Should see: `note_a.txt note_b.txt note_cc.txt`
    
7. Check a path pattern:
    
    ```bash
    ls /home/user/note_[12].txt
    ```
    
    If those files exist, it’ll list them.
    
8. Clean up:
    
    ```bash
    rm note_*
    ```
    

#practice

---
