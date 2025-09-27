# Piping~redirecting-output
The challenge’s purpose was  redirecting standard output to files which can be accomplished by the the > character.

## My solve
**Flag:** ` pwn.college{ICb6gQxs_-06qo_SKc_kxiOGc5V.QX0YTN0wiN5gjNzEzW}`

### Thought process/Steps
The steps were straightforward. I had to redirect the output of echo PWN (which only prints PWN) into a particular file, 
so I used > after my command to get it done.

 ```bash
~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{ICb6gQxs_-06qo_SKc_kxiOGc5V.QX0YTN0wiN5gjNzEzW}```
