# Backgrounding-processes
The challenge’s purpose was to make us learn how to resume suspended cmds  in the background  using the bg cmd feature.

**Flag:** ` pwn.college{8ovMsh8v1xwx73V7-gjO7qdm3DH.QX3QDO0wiN5gjNzEzW}`

### Thought Process/Steps
The steps were simple and straightforward. The question mentioned that I had to run /challenge/run and then suspend it using 
CTRL+Z, which pauses the process and keeps it in the background in a stopped state. After suspending /challenge/run, 
I resumed it in the background (not the foreground) by typing bg. Once it was running in the background, I got my shell back, and 
in that shell, I invoked /challenge/run again to get my flag.


 ```bash
~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         138 S+   bash /challenge/run
root         140 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         138 S    bash /challenge/run
root         148 S    sleep 6h
root         149 S+   bash /challenge/run
root         151 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{8ovMsh8v1xwx73V7-gjO7qdm3DH.QX3QDO0wiN5gjNzEzW}```
