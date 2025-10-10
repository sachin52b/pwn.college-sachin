# ADDING-COMMANDS
The challenge purpose was to make us learn how the PATH variable controls command lookup and why supplying a custom win script 
(so a root-run program can find and execute it) reveals the flag.

## MY SOLVE
**Flag:** ` pwn.college{gdS6pYofLTEFkMh_IcnSe0Nyo9l.QX2cjM1wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
At first I tried to think through how to make this work: /challenge/run will call a bare win command, so I needed to create a win 
script that reads /flag, and I also knew I would have to change PATH so /challenge/run could find my win. The tricky part was that 
if I overwrite PATH then cat might not be found anymore, so I had to make cat usable inside my win even after changing PATH.
So I started by creating the script file with nano win and planning to put cat /flag inside it — but that alone wouldn’t survive 
overwriting PATH. To avoid relying on PATH, I ran which cat to get cat’s full absolute path. Once I had that path, I edited win 
and put a line that called the absolute cat (for me that was /run/dojo/bin/cat /flag), so the script would work without needing PATH.
Next I made sure win could be executed by other users (including root), because /challenge/run runs as root. I changed the file’s 
permissions with chmod so it was executable. Then I overwrote PATH to point to the directory where I saved win (PATH=/home/hacker), 
so when /challenge/run invoked win by its bare name it would find my script. Finally I invoked /challenge/run, and because my win 
used the absolute cat path, it printed the flag.some other methods were also listed in the challenge's description but i figured out
the above method on my own. 

```bash
~$ which cat
/run/dojo/bin/cat
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ chmod o+x win
hacker@path~adding-commands:~$ PATH=/home/hacker/
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{gdS6pYofLTEFkMh_IcnSe0Nyo9l.QX2cjM1wiN5gjNzEzW}
```
