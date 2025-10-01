# Commands~making-directories

This challenge expected us to make a new folder/directory using mkdir cmd.

## My solve
**Flag:** `pwn.college{o6n-9KLxxi22B9F0R9-n1R82mFy.QXxMDO0wiN5gjNzEzW}`

### Thought process
basic use of mkdir command to create a folder then use of touch command to create a file in the new directory just created the 
path had to passed as argument in mkdir to make a folder then passing the path with a further filename college to create the file.




```bash
~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ touch /tmp/pwn/college
hacker@commands~making-directories:~$ /challenge/run
Success! Here is your flag:
pwn.college{o6n-9KLxxi22B9F0R9-n1R82mFy.QXxMDO0wiN5gjNzEzW}```
