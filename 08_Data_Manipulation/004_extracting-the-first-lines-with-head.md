# Extracting-the-first-lines-with-head
The challenge’s purpose was to make us learn how to use head to just get the starting few lines (of the stdinput to the head cmd).

## My solve
**Flag:** ` pwn.college{UOgiiER3o0C3GnRzUZilqYRbk22.0lNxEzNxwiN5gjNzEzW}`

### Thought process/Steps
The steps were basic and straight forward first I used | to convert the standard output of /challenge/run cmd to standard input for head 
then I used (head –n  no_of_lines) to just get the first 7 lines as the output then I again piped this to another cmd which finally gave me the flag.

 ```bash
:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{UOgiiER3o0C3GnRzUZilqYRbk22.0lNxEzNxwiN5gjNzEzW} ```
