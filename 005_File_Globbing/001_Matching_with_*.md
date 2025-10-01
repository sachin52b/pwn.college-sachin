# Matching_with_*
The challenge’s purpose was to learn how to use * for globbing .

## My solve
**Flag:** ` pwn.college{UmQwaEP5fXjO172Tk_1HDVVqYDC.QXxIDO0wiN5gjNzEzW}`

### Thought process/Steps
First I had to use cd cmd to get into the challenge directory but argument had to be only 4 characters thus the use of * came in, 
once into the directory I had to invoke a simple cmd to get the flag.

```bash
~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{UmQwaEP5fXjO172Tk_1HDVVqYDC.QXxIDO0wiN5gjNzEzW}```
