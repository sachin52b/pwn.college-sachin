# Catting-absolute-paths

This challenge expected us to read a file through cat command. 

## My solve
**Flag:** `pwn.college{c5BFWemGnBPve7hDnT3G5kF5IC-.QXwITO0wiN5gjNzEzW}`

### Thought process

There wasn't actually much just had to read a file named 'flag' using cat cmd but this time through absolute path(the flag was not directly in home directory but a particular directory was given to us already we had to just write cat path_given.)



```bash
~$ cat /lib/ssl/flag
pwn.college{c5BFWemGnBPve7hDnT3G5kF5IC-.QXwITO0wiN5gjNzEzW}```
