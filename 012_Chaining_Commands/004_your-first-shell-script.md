# YOUR-FIRST-SHELL-SCRIPT
The challenge expected us to now write our commands in shell script and then execute it .

## MY SOLVE
**Flag:** `  pwn.college{89Gc1T7JTy770y16ar5h89sydCG.QXxcDO0wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
The challenge pointed out that long one-liners can get messy, and the clean fix is to put the commands into a script and run that 
instead. I figured I’d make a tiny shell file — the challenge didn’t show how to create one, but the markdown exercises had me 
thinking of nano, so I opened nano x.sh and wrote the two commands:
/challenge/pwn
/challenge/college
I needed to run. I saved the file and executed it with bash x.sh (the description confirmed that’s how it’s done). Running the 
script executed both commands in order and gave me the flag.

```bash
 ~$ nano x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{89Gc1T7JTy770y16ar5h89sydCG.QXxcDO0wiN5gjNzEzW}
```
