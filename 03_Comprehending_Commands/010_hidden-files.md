# Hidden-files:

This challenge expected us to read a hidden file to find a flag

## My solve
**Flag:** `pwn.college{klZhmO4-sSoWMsfJ-jynapLBGrq.QXwUDO0wiN5gjNzEzW}`

### Thought process/Procedure
First I had to use ls -a / to get the list of all files including hidden files there was the flag file I finally read the file through cat command 
in order to get the flag




```bash
:~$ ls -a /.
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-13203738417638  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ cat /.flag-13203738417638
pwn.college{klZhmO4-sSoWMsfJ-jynapLBGrq.QXwUDO0wiN5gjNzEzW}```
