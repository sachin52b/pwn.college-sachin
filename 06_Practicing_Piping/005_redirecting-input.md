# Redirecting-input
The main goal of the challenge was to learn how input redirection works in Linux and how programs can read data directly 
from files.

## My solve
**Flag:** `  pwn.college{0-s4MbtqRELNZI2vSyhnFvCyUDS.QXwcTN0wiN5gjNzEzW}`

### Thought process/Steps
In the challenge I had to put the word COLLEGE into a file and then give that file as input to /challenge/run using 
< so I first used output redirection to get COLLEGE into a file and then I used > to take the input from the same file.

 ```bash
~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{0-s4MbtqRELNZI2vSyhnFvCyUDS.QXwcTN0wiN5gjNzEzW}```
