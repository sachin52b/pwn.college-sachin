# Matching_with_[]
The challenge’s purpose was to learn how to use [] for globbing .

## My solve
**Flag:** ` pwn.college{Uef8f_DqilXK_uWfYr9uirZ3BYT.QXzIDO0wiN5gjNzEzW}`

### Thought process/Steps
First, I had to use the cd command to get into /challenge/files. Then, I had to invoke /challenge/run with a single argument 
such that all files (bash) are included as arguments when the system expands it. Here, the use of [] allows us to define a set of 
characters (bash), so that after expansion, all matching files are passed as arguments.

```bash
~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{Uef8f_DqilXK_uWfYr9uirZ3BYT.QXzIDO0wiN5gjNzEzW}```
