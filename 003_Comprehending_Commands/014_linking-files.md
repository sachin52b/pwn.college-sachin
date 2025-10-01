# Linking-files

This challenge expected use a symlink in order to get the flag

## My solve
**Flag:** `pwn.college{wn0IargdqdzE5LrVG4zA98gbsX_.QX5ETN1wiN5gjNzEzW}`

### Thought process
The program /challenge/catflag was reading /home/hacker/not-the-flag, which wasn’t the real flag. I realized I could use a symbolic link to point /home/hacker/not-the-flag to /flag. Then, when the program ran, it followed the link and gave me the actual flag without changing the program itself


```bash
~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{wn0IargdqdzE5LrVG4zA98gbsX_.QX5ETN1wiN5gjNzEzW}```
