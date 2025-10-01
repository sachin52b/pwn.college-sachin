# Explicit-relative-paths-from

This challenge expected us to first change directory then execute the desired file but this time using explicit relative paths i.e "./"

## My solve
**Flag:** `pwn.college{s-7rxP7pvOV9BB_mbB-gsn8bbAR.QXwUTN0wiN5gjNzEzW}`

to solve the challenge I had to go into a directory / which I went into through cd and then execute the file with use of relative path ./challenge/run so I basically used cd to get
into / and then simply executed the run file by typing the relative path "./challenge/run". 

In this challenge thought process was clear that we don't have to use challenge/run but explicitly mention that its a relative path meaning use of "./"


```bash
~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{s-7rxP7pvOV9BB_mbB-gsn8bbAR.QXwUTN0wiN5gjNzEzW}```
