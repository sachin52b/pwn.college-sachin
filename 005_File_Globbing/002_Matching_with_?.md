# Matching_with_?
The challenge’s purpose was to learn how to use ? for globbing .

## My solve
**Flag:** ` pwn.college{kExHUj7DEwZILE7EEIvr0jlyj0w.QXyIDO0wiN5gjNzEzW} `

### Thought process/Steps
First I had to use cd cmd to get into the challenge directory but argument I was only allowed to do that if instead of c and l 
I used ? (? Works for single character). Once I was in the correct directory I invoked the req command to get the flag.


```bash
~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{kExHUj7DEwZILE7EEIvr0jlyj0w.QXyIDO0wiN5gjNzEzW} ```
