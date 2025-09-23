# position-elsewhere

This challenge expected us to first change or directory then execute the desired file

## My solve
**Flag:** `pwn.college{wuMz7K3KoIXvO1DztKGNLvPOswi.QX3QTN0wiN5gjNzEzW}`

to solve the challenge I had to go into a directory /proc/131/fd and then execute the file with use of absolute path /challenge/run so I basically used cd to get
into proc/131/fd and then simply executed the run file by typing the exact path "/challenge/run".

```bash
~$ /challenge/run
Incorrect...
You are not currently in the /proc/131/fd directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /proc/131/fd
hacker@paths~position-elsewhere:/proc/131/fd$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{wuMz7K3KoIXvO1DztKGNLvPOswi.QX3QTN0wiN5gjNzEzW}```
