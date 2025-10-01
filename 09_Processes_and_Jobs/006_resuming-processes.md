
# Resuming-processes.
The challenge’s purpose was to make us learn how to resume suspended cmds using the fg cmd feature.

**Flag:** ` pwn.college{UzyIg367EVoGWSxtQDtRLOOBgWI.QX2QDO0wiN5gjNzEzW} `

### Thought Process/Steps
The steps were simple and straightforward. The question mentioned that I had to run /challenge/run and then suspend it using 
CTRL+Z, which pauses the process and keeps it in the background in a stopped state. After suspending /challenge/run, I had to resume 
it by typing in fg, once resumed it provided me with the flag.

 ```bash
~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{UzyIg367EVoGWSxtQDtRLOOBgWI.QX2QDO0wiN5gjNzEzW}
Don't forget to press Enter to quit me!

Goodbye!```
