# FINDING-COMMANDS
The challenge’s purpose was to introduce us to which command, explain its working and applying it for the task.

## MY SOLVE
**Flag:** ` pwn.college{QT5FJPCf0kwJxUtl1NwC99Qte-l.01NzEzNxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
In this challenge, I first learned what the which command does. It searches through all the directories listed in the PATH variable 
to find the location of the file or command name given as an argument, and then returns its full path.
The challenge mentioned that the flag file was in the same directory as the win command. So, I figured I should first find where 
win was located. I ran:
which win
This gave me the full path:
/challenge/paths/16257/win
From that, I understood that the flag file would be in the same folder — /challenge/paths/16257. So its full path would be:
/challenge/paths/16257/flag
I then used that path with the cat command:
cat /challenge/paths/16257/flag
And that finally displayed the flag.

```bash
~$ which win
/challenge/paths/16257/win
hacker@path~finding-commands:~$ cat /challenge/paths/16257/flag
pwn.college{QT5FJPCf0kwJxUtl1NwC99Qte-l.01NzEzNxwiN5gjNzEzW}
```

