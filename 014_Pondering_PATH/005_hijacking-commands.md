
# HIJACKING-COMMANDS
The challenge expected us to figure out a way to /challenge/run give our flag.

## MY SOLVE
**Flag:** ` pwn.college{cS30vw5C3v_PG4AELaBBXAzu5Eg.QX3cjM1wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
This wasn’t a one-shot for me — I had to try a few things before I really understood what the challenge wanted. To start with a 
blank slate and see the exact behavior, I simply ran /challenge/run. It printed:
“Trying to remove /flag...
Found 'rm' command at /run/dojo/bin/rm. Executing!
Uh oh, looks like I successfully removed the flag! That means you did not properly set PATH to keep me from finding 'rm'. Since the 
flag is gone, you will need to re-launch the challenge from the module page! Better luck next time.”
Seeing that made the whole point click: when /challenge/run runs it looks for an rm command and it found one at 
/run/dojo/bin/rm — and that was only possible because my PATH included that directory. So the goal became clear: make 
/challenge/run find my rm instead of the system one. If the shell finds only a single rm — one I control — I can make that rm do 
whatever I want.
I followed the same initial trick as before: I ran which cat to get the absolute path to cat so I wouldn’t depend on PATH later. 
Then I created a file called rm with nano rm and put a simple line in it that uses the absolute cat to read the flag:
/run/dojo/bin/cat /flag
Basically, my fake rm just prints the flag instead of deleting it. Next I made it executable for other users (including root) with 
chmod, because /challenge/run runs as root and needs to be able to execute my rm without permission problems. Finally, I overwritten 
PATH to point to the directory where my rm lived (for me, PATH=/home/hacker/rm). Now, when I invoked /challenge/run, the shell 
searched PATH for rm, found my fake rm, and executed it — which used cat to show /flag. That tricked /challenge/run into 
"removing" the flag by actually printing it, and I got the flag.


```bash
~$ which cat
/run/dojo/bin/cat
hacker@path~hijacking-commands:~$ nano rm
hacker@path~hijacking-commands:~$ chmod o+x rm
hacker@path~hijacking-commands:~$ PATH=/home/hacker/
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
pwn.college{cS30vw5C3v_PG4AELaBBXAzu5Eg.QX3cjM1wiN5gjNzEzW}
```
