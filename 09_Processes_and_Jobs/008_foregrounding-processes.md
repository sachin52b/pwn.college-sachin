
# Foregrounding-processes
The challenge’s purpose was to make us learn how to get the backgrounded processes again come on the foreground .

**Flag:** ` pwn.college{o-l7OcvxHqpRRevJjLVZKERuhR4.QX4QDO0wiN5gjNzEzW}`

### Thought Process/Steps
The steps were simple and straightforward. The question mentioned that I had to run /challenge/run and then suspend it using 
CTRL+Z, which pauses the process and keeps it in the background in a stopped state. After suspending /challenge/run, I resumed it 
in the background (not the foreground) by typing bg. Once it was running in the background, I got my shell back, and in that shell,
I invoked fg cmd to get the backgrounded process back to foreground .

 ```bash
$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and *then* foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.

hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{o-l7OcvxHqpRRevJjLVZKERuhR4.QX4QDO0wiN5gjNzEzW}```
