
# SWITCHING WINODWS
The challenge’s purpose was to make us learn how to switch between different windows of screen.

## MY SOLVE
**Flag:** ` pwn.college{8fTd5kcdAzWPcgWQMwrPtuVAFEk.0FO4IDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
I first reattached the screen with screen -r. 

```bash
:~$ screen -r
```

That was simple — the real trick was that this screen had multiple windows (two in this case). When I reattached I landed on 
window 1, but the challenge hinted the flag was on window 0, so I needed to switch. The prompt itself explained how to create 
windows, open the window menu, or jump to a numbered window. I switched to window 0 by pressing Ctrl+a then 0, and there I found 
the flag. (Because there were only two windows, I could also have pressed Ctrl+a then n to move to the previous window, or Ctrl+a 
then " to open the window menu and pick window 0.)
