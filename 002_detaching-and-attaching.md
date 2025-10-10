# DETACHING-AND-ATTACHING
The challenge’s purpose was to make us learn how to detach and attach a screen.

## MY SOLVE
**Flag:** ` pwn.college{AU3bkBr6B9riWNcEftS4gdnrf88.0lN4IDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
I had to use the screen command to open a new screen session. To detach it (keep it running in the background and return to my 
normal terminal), I first pressed Ctrl+a to activate screen’s shortcuts, then pressed d to detach. Back at my regular shell, I 
ran /challenge/run, which sent the flag to the detached screen. To see it, I reattached with screen -r and found the flag.

```bash
~$ screen
[detached from 195.pts-0.terminal-multiplexing~detaching-and-attaching]
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run
Found detached screen session: 195.pts-0.terminal-multiplexing~detaching-and-attaching
Sending flag to your screen session...

Flag sent! Now reattach to your screen session with:

  screen -r

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen –r
```
