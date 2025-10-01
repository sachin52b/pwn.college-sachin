# Killing-processes
The challenge’s purpose was to make us learn to terminate processes using the kill command.

## My solve
**Flag:** ` pwn.college{Efw5O1mRZMOYODtWMDIFxL4_D7i.QXyQDO0wiN5gjNzEzW}} `

### Thought Process/Steps
The steps were simple and straightforward. The question mentioned that we had to run /challenge/run, but the twist was that 
another process /challenge/don’t_run was running, which prevented /challenge/run from launching. So, our goal was to kill the 
/challenge/don’t_run process. For that, I used ps -ef to list all processes, then grabbed the PID of /challenge/don’t_run 
and used kill PID to terminate it. After that, I invoked /challenge/run to get my flag.

 ```bash
~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 10:43 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo
root           7       1  0 10:43 ?        00:00:00 /run/dojo/bin/sleep 6h
root         135       1  0 10:43 ?        00:00:00 su -c /challenge/.launcher hacker
hacker       136     135  0 10:43 ?        00:00:00 /challenge/dont_run
hacker       137     136  0 10:43 ?        00:00:00 sleep 6h
hacker       139       0  0 10:44 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run
hacker       145     139  0 10:44 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       154     145  0 10:44 pts/0    00:00:00 ps -ef
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{Efw5O1mRZMOYODtWMDIFxL4_D7i.QXyQDO0wiN5gjNzEzW} ```
