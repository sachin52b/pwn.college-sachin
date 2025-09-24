# Position yet elsewhere

This challenge expected us to first change directory then execute the desired file

## My solve
**Flag:** `pwn.college{QUSAFn0dCgSDhjH3pJZO9yCNjJr.QX4QTN0wiN5gjNzEzW}`

to solve the challenge I had to go into a directory /usr/share/doc and then execute the file with use of absolute path /challenge/run so I basically used cd to get
into /usr/share/doc and then simply executed the run file by typing the exact path "/challenge/run".

```bash
~$ cd /usr/share/doc
hacker@paths~position-yet-elsewhere:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{QUSAFn0dCgSDhjH3pJZO9yCNjJr.QX4QTN0wiN5gjNzEzW}```
