# Position thy self

This challenge expected us to first change or directory then execute the desired file

## My solve
**Flag:** `pwn.college{Iwvf6Z7aZ7lwZEkM6cfm0pGGFNd.QX2QTN0wiN5gjNzEzW}`

to solve the challenge I had to go into a directory /var and then execute the file with use of absolute path /challenge/run so I basically used cd to get
into var and then simply executed the run file by typing the exact path "/challenge/run".
(first I was not getting to change into which directory so I directly tyoed /challenge/run then it showed me incorrect you have to execute from inside of /var
then I was easily able to use cd and do my further process)

```bash
~$ cd /var
hacker@paths~position-thy-self:/var$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Iwvf6Z7aZ7lwZEkM6cfm0pGGFNd.QX2QTN0wiN5gjNzEzW}```

