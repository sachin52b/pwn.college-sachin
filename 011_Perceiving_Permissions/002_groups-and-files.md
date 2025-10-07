# GROUPS-AND-FILES
The challenge expected to us to learn and implement how to change the group ownership of a file.

## MY SOLVE
**Flag:** ` pwn.college{gS87AVC-BQ4cDY0sEbFqW9dNppx.QXxcjM1wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
I was told that chgrp (change group) changes a file’s group, but that chgrp can normally only be used as root. Root is like the 
system’s admin, so I thought I’d need extra privileges. For convenience in this challenge, however, chgrp could be run as the hacker 
user. My goal was to change the group of /flag from root  to hacker so I could run cat /flag without a permission denied error. 
I used chgrp hacker /flag to change the file’s group, for confirmation I used ls –l for /flag file to see the change that was made 
and then ran cat /flag to read the flag.

```bash
~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ ls -l /flag
-r--r----- 1 root hacker 60 Oct  7 08:13 /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{gS87AVC-BQ4cDY0sEbFqW9dNppx.QXxcjM1wiN5gjNzEzW}
```
