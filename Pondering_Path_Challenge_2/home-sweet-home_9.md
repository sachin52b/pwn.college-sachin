# Home-sweet-home

This challenge expected us to copy the flag through /challenge/run into a path passed as an argument in the same. 

## My solve
**Flag:** `pwn.college{UABItq8VxuszN11lgY_65MFgyj-.QXzMDO0wiN5gjNzEzW}`

###Thought process

To solve the challenge I had to pass a condition-appropriate argument. The conditions were listed in the challenge the path had to be 3 letters or less, it had to be in home and had to be absolute not relative ie starting from /. only way to do it was to use shorthand of /home/username that is basically ~ 
~/ goes into the folder then finally ~/some_file_name would be the final path to the file in which the flag has to be copied 



```bash
~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{UABItq8VxuszN11lgY_65MFgyj-.QXzMDO0wiN5gjNzEzW}```
