# FINDING-SESSIONS
The challenge’s purpose was to make us learn how to reattach to a particular screen when ultiple screens are running.

## MY SOLVE
**Flag:** ` pwn.college{UKhMb1iZ-uoI9wjY4nNC_NP2HUR.01N4IDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
In the challenge I was told how to list the screen sessions currently running — just run screen -ls. That shows all sessions and 
their PIDs, so to reattach you use screen -r with the PID of the session you want to resume (for example screen -r 1234).
For this task I listed the screens with screen -ls and then tried screen -r with different PIDs until I found the right one. I 
eventually found the flag on the second screen I checked.

```bash
:~$ screen -ls
There are screens on:
        150.pts-0.terminal-multiplexing~launching-screen        (Remote or dead)
        144.session_3a055b3a9ba1deff    (Detached)
        147.session_c7a0c4ae8fa445a8    (Detached)
        150.session_a085705e4aae6c85    (Detached)
4 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 144
[detached from 144.session_3a055b3a9ba1deff]
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 147
[detached from 147.session_c7a0c4ae8fa445a8]
```
