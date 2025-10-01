# Matching_with_[]
The challenge’s purpose was to learn how to use [] for globbing  but this time with the path.

## My solve
**Flag:** ` pwn.college{gy4JHAkOTs5Jc_v3Iow7q3mVZcB.QX0IDO0wiN5gjNzEzW}

### Thought process/Steps
First, I had to use the cd command to get into /challenge/files. Then, I had to invoke /challenge/run with a single argument such 
that all files (bash) are included as arguments when the system expands it.  Here, the use of [] allows us to define a set of 
characters (bash), so that after expansion, all matching files are passed as arguments. Only difference was this time I had to 
mention the path as well .

```bash
~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{gy4JHAkOTs5Jc_v3Iow7q3mVZcB.QX0IDO0wiN5gjNzEzW}```
