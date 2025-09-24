# Implicit-relative-path

This challenge expected us to first change directory then execute the desired file 

## My solve
**Flag:** `pwn.college{UBcZ2mpn81Fsfyw-CwbytECwZd6.QXxUTN0wiN5gjNzEzW}`

to solve the challenge I had to go into a directory /challenge which I went into through cd and then execute the file with use of relative path ./run so I basically used cd to get
into /challenge and then simply executed the run file by typing the relative path ".run". 

In this challenge thought process was clear that we have to first go into the directory desired through cd command now the thing was to get iinto the challenge directory and directly execute run file so first we went totally into challenge by using cd /challenge now to execute the run file we couldn't write run directly we have to use explicit relative path to specify to Linux to execute file from challenge(which is the current directory) only.


```bash
:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{UBcZ2mpn81Fsfyw-CwbytECwZd6.QXxUTN0wiN5gjNzEzW}```
