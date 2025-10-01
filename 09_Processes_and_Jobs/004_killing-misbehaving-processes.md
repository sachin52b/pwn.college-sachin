
# Killing-misbehaving-processes
The challenge’s purpose was to make us learn how to kill misbehaving processes.

**Flag:** ` pwn.college{IJ-7zToYrrFcHpj_Y5t51pdPHe2.0FNzMDOxwiN5gjNzEzW} `

### Thought Process/Steps
The steps were simple and straightforward. The question mentioned that I had to run /challenge/run, which outputs the flag into a
FIFO. Before doing this, I first had to kill a process that was generating decoy flags. So, I used ps -ef to list the processes and 
then used kill PID to terminate the decoy process. After that, I invoked /challenge/run, which wrote the output to the FIFO. In 
another terminal, I used cat to read from the FIFO. At first, I saw some decoy flags, but once I ran /challenge/run again in the 
first terminal, I finally got the correct flag in the other terminal.

#TERMINAL 1
 ```bash
~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 11:09 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo
root           7       1  0 11:09 ?        00:00:00 /run/dojo/bin/sleep 6h
root         137       1  0 11:09 ?        00:00:00 /bin/bash /challenge/.init
root         138       1  0 11:09 ?        00:00:00 /bin/bash /challenge/.init
root         139       1  0 11:09 ?        00:00:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         140     138  0 11:09 ?        00:00:00 sleep 6h
root         141     137  0 11:09 ?        00:00:00 sleep 6h
hacker       142     139  0 11:09 ?        00:00:00 /usr/bin/python /challenge/decoy
hacker       144       0  0 11:09 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run
hacker       150     144  0 11:09 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       168       1  2 11:09 ?        00:00:00 /nix/store/a1kxazxkgw7mjbjgisvah95p1r3n5ykl-nodejs-22.16.0/bin/node /nix/store/5h
hacker       191     168  5 11:09 ?        00:00:01 /nix/store/a1kxazxkgw7mjbjgisvah95p1r3n5ykl-nodejs-22.16.0/bin/node /nix/store/5h
hacker       213     150  0 11:09 pts/0    00:00:00 ps -ef
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!```

#TERMINAL 2
```bash
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
DECCOY FLAGS SHOWN…..
pwn.college{IJ-7zToYrrFcHpj_Y5t51pdPHe2.0FNzMDOxwiN5gjNzEzW}
After running /challenge/run again on TERMINAL 1
pwn.college{IJ-7zToYrrFcHpj_Y5t51pdPHe2.0FNzMDOxwiN5gjNzEzW}```

