# Implicit-relative-paths-from

This challenge expected us to first change directory then execute the desired file

## My solve
**Flag:** `pwn.college{sZ2aAHJB7npMvqz_CZlYXlveC5p.QX5QTN0wiN5gjNzEzW}`

to solve the challenge I had to go into a directory / which I went into through cd and then execute the file with use of relative path challenge/run so I basically used cd to get
into / and then simply executed the run file by typing the relative path "challenge/run". 
(I faced some issues but finally figured it the thing like first I didnt know which directory to start from so experimentally I just used /challenge/run then after it showed error it srtiked me that we had to start from root directory i.e / then I just typed in the relative path challenge/run as a hint was also given that relative path starts from c

```bash
:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{sZ2aAHJB7npMvqz_CZlYXlveC5p.QX5QTN0wiN5gjNzEzW}```
