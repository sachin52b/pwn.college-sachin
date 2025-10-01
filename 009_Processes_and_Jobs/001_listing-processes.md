
# Listing-processes
The challenge’s purpose was to make us learn to list all the processes using the ps cmd. Main uses learnt were ps -ef and ps -aux.

## My solve
**Flag:** ` pwn.college{8NHKFd-ZgfhzfM74ZKwg08Ae-2c.QX4MDO0wiN5gjNzEzW} `

### Thought process/Steps
The steps were simple and straightforward. The question mentioned that we had to run /challenge/run, but the twist was that it 
had been renamed and could only be invoked using its correct name, not /challenge/run. However, it was also stated that the 
program was already running as a process. So, I used ps -ef to list all processes, found the new name of /challenge/run, and then 
invoked it to get the flag.

 ```bash
~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 10:28 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo
root           7       1  0 10:28 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 10:28 ?        00:00:00 /challenge/29757-run-29444
root         135     132  0 10:28 ?        00:00:00 sleep 6h
hacker       137       0  0 10:29 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run
hacker       143     137  0 10:29 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       152     143  0 10:29 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/29757-run-29444
Yahaha, you found me! Here is your flag:
pwn.college{8NHKFd-ZgfhzfM74ZKwg08Ae-2c.QX4MDO0wiN5gjNzEzW}```
