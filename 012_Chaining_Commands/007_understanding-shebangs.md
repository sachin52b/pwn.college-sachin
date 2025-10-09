# UNDERSTANDING-SHEBANGS
The challenge’s purpose was to make us understand the concept of she-bangs and the use of it.

## MY SOLVE
**Flag:** `  pwn.college{U37tBNKeHxVIvrT_WefCtxUCLCG.0VOzMDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
At first, I wasn’t really sure what a shebang was—honestly, the whole #! thing at the top of scripts always kind of confused me. 
But this challenge started to clear things up. I realized it’s just a way of telling Linux what program should run the script.  So, 
I opened Nano and started a script named `script_name.sh`. I paused for a second, thinking about what to put first—and then 
remembered, right, the shebang line goes at the top. I typed it out, almost out of habit now, and then dropped in the simple 
command: `echo hack-the-planet`. That part made sense—I knew it would just print out the phrase if everything worked.But as soon 
as I saved the file, it hit me: Linux probably won’t let me run this unless I actually make it executable. I always forget that 
part. So I used `chmod u+x z.sh`—still have to remind myself what the flags mean, but I’ve used it enough times now that it’s 
almost muscle memory. After that, I needed to check if the challenge would accept my solution, so I ran `/challenge/run` which checked if everything was done perfectly and gave me the flag.
 
```bash
~$ nano solve.sh
hacker@chaining~understanding-shebangs:~$ chmod u+x solve.sh
hacker@chaining~understanding-shebangs:~$  /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{U37tBNKeHxVIvrT_WefCtxUCLCG.0VOzMDOxwiN5gjNzEzW}
```
