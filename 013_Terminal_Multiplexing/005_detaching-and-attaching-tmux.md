# DETACHING-AND-ATTACHING-TMUX
The challenge’s purpose was to make us learn how to launch,detach and reattach a 
tmux(terminal multiplexer) .

## MY SOLVE
**Flag:** ` pwn.college{w8eihDNEw4D0BX798gtqt7fqUHb.0VO4IDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
First, I launched a tmux session by simply running the tmux command — it works quite similarly to screen. The main difference between 
the two is the shortcut key: in screen, we use Ctrl+a for shortcuts, while in tmux, it’s Ctrl+b.
To detach from the session, I pressed Ctrl+b followed by d, which brought me back to my normal terminal while keeping the tmux 
session running in the background. Then I executed /challenge/run, which sent the flag to the tmux session. To get back to it, I 
used the tmux a command (as mentioned in the challenge instructions). Once I reattached, I found my flag inside the tmux session.

```bash
~$ tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux a
```
