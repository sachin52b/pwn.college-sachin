
# THE-PATH-VARIABLE
The challenge’s purpose was to make us learn about a special shell variable, called PATH, that stores a bunch of directory paths in 
which the shell will search for programs corresponding to commands.

## MY SOLVE
**Flag:** ` pwn.college{oSDZ7n2y10uyarnsCcnc5_q_RYO.QX2cDM1wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
In this challenge, I was introduced to the PATH variable. The task was to disrupt the /challenge/run command. Normally, when I ran 
/challenge/run, it would execute the rm command and delete the flag.txt file. So my goal was to make the rm command useless — in 
other words, make the system unable to find it.
That’s when I realized the PATH variable plays a key role here. It stores a list of directory paths where the shell looks for 
executable programs whenever a command is run. If I cleared this variable, the shell wouldn’t know where to find commands like 
rm. So I set:
PATH=""
After that, when I ran /challenge/run, the shell couldn’t locate rm, and as a result, the file wasn’t deleted. That’s how I got my 
flag.

```bash
:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{oSDZ7n2y10uyarnsCcnc5_q_RYO.QX2cDM1wiN5gjNzEzW}
```


