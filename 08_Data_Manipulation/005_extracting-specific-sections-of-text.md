# Extracting-specific-sections-of-text
The challenge’s purpose was to make us explore the use of cut command. 

## My solve
**Flag:** ` pwn.college{EP_fL3Id5352-MN4WNWjpL6_02f.01NxEzNxwiN5gjNzEzW}`

### Thought process/Steps
The steps were simple and straightforward. First, I used | to send the standard output of the /challenge/run command into the cut command. 
The cut command requires two main arguments: -d to specify the delimiter (the character separating the columns) and -f to
indicate which column to extract. After that, I piped the output of cut into the tr command to remove newlines, which finally 
gave me the flag

 ```bash
~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{EP_fL3Id5352-MN4WNWjpL6_02f.01NxEzNxwiN5gjNzEzW} ```
