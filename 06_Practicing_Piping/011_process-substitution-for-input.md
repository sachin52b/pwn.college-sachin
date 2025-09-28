# Process-substitution-for-input
This challenge shows how the shell can treat a program’s live output like a temporary file, so two command outputs can be 
compared directly.
Its purpose is to demonstrate a cleaner way to find differences (like a real flag hidden among decoys) without making extra files, 
highlighting powerful shell shortcuts.

## My solve
**Flag:** `  pwn.college{kgt7ttTFVgI27UJiD2JUqlCzQXa.0lNwMDOxwiN5gjNzEzW}`

### Thought process/Steps
In this challenge I used process substitution so I could run diff on two commands. Since diff accepts only filenames, <(...) converted 
each command’s output into a temporary file-like stream, allowing the comparison to be done in a single line.

 ```bash
~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
49a50
> pwn.college{kgt7ttTFVgI27UJiD2JUqlCzQXa.0lNwMDOxwiN5gjNzEzW}```

