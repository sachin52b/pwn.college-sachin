# Man~searching-manuals
The challenge expected us to search in the manual in order to get the argument to be used to further get the flag.

## My solve
**Flag:** ` pwn.college{EGfhlOPuWf89vh4nF5TMj1D1p9l.QX1EDO0wiN5gjNzEzW}`

### Thought process/Steps
The task was to just write man cmd for challenge so that the manual opens, the manual opened and it had the instructions on how to get the 
flag(it was by using a particular argument.Next I used / to search for flag then pressed n to move to the lines with flag in them eventually 
I found the argument to be used)

```bash
~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --mjvlkya
Initializing...
Correct usage! Your flag: pwn.college{EGfhlOPuWf89vh4nF5TMj1D1p9l.QX1EDO0wiN5gjNzEzW}```
