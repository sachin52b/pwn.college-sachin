# CHANGING-FILE-OWNERSHIP
The challenge expected to us to learn and implement how to change the owner of a file.

## MY SOLVE
**Flag:** ` pwn.college{kFTg4PCNbLyGwxyKon45Qv1I2Nf.QXxEjN0wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
I was told that chown (change owner) changes a file’s owner, but that chown can normally only be used as root. Root is like the 
system’s admin, so I expected I’d need extra privilege. For convenience in this challenge, however, chown could be run as the 
hacker user. My goal was to change the owner of /flag from root to hacker so I could run cat /flag without a permission denied 
error. I used chown hacker /flag to change the file’s owner, then ran cat /flag to read the flag.


```bash
:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{kFTg4PCNbLyGwxyKon45Qv1I2Nf.QXxEjN0wiN5gjNzEzW}
```
