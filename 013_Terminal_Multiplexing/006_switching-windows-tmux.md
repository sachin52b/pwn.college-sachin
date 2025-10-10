# SWITCHING-WINDOWS-TMUX
The challenge’s purpose was to make us learn how to switch windows in a tmux. 

## MY SOLVE
**Flag:** ` pwn.college{ABA9DODHcisrFYykNbsbDxtPZ3o.0FM5IDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
This challenge felt quite similar to Challenge 4 — the only difference was that this time I had to switch windows inside a tmux 
session instead of a screen session. The controls were already explained in the challenge description; I just had to follow them. 
Once again, I was asked to go to window 0 to find the flag.
I started by reattaching to the tmux session using the tmux a command.
```bash
~$ tmux a
```
After getting back in, I tried a slightly different approach instead of switching directly by number. I used the window picker — I 
pressed Ctrl+b followed by w (as mentioned in the question). This opened a list of all windows, and I could move through them 
using the Page Up/Page Down or arrow keys. I navigated to window 0 and found my flag there.
