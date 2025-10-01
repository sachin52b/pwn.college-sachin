# Suspending-processes.
The challenge’s purpose was to make us learn how to suspend  processes to background using CTRL+Z.

**Flag:** ` pwn.college{sQ4prwyr2BydJlS3kdd3FT3IGym.QX1QDO0wiN5gjNzEzW} `

### Thought Process/Steps
The steps were simple and straightforward. The question mentioned that I had to run /challenge/run and then suspend it using 
CTRL+Z, which pauses the process and keeps it in the background in a stopped state. After suspending /challenge/run, I had to 
invoke it again so that this command detected another version of itself running in the background, which then gave me the flag.
 

```bash
~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         154     144  0 11:24 pts/1    00:00:00 bash /challenge/run
root         156     154  0 11:24 pts/1    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         154     144  0 11:24 pts/1    00:00:00 bash /challenge/run
root         161     144  0 11:24 pts/1    00:00:00 bash /challenge/run
root         163     161  0 11:24 pts/1    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{sQ4prwyr2BydJlS3kdd3FT3IGym.QX1QDO0wiN5gjNzEzW}```

