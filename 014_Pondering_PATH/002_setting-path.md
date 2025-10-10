# SETTING-PATH
The challenge’s purpose was to make us use PATH variable for something useful like instead of disrupting a cmd use it for adding a 
new cmd.

## MY SOLVE
**Flag:** ` pwn.college{8_Ck7SiBcZiPAPbmevzB6D8QBZU.QX1cjM1wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
In this challenge, /challenge/run tried to run the win command by its bare name, but my PATH didn’t include the directory where 
win lived — so invoking /challenge/run wouldn’t find win and would fail. I was given the directory that contained the win command, 
so I simply updated PATH to include it. I did:
PATH=/challenge/more_commands/
After that, running /challenge/run worked because the shell could find win by its bare name. Everything ran correctly and I got 
the flag.

```bash
~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{8_Ck7SiBcZiPAPbmevzB6D8QBZU.QX1cjM1wiN5gjNzEzW}
```
