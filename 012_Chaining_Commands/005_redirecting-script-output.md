# REDIRECTING-SCRIPT-OUTPUT
The challenge expected us to now write our commands in shell script and then pipe it using |.

## MY SOLVE
**Flag:** `  pwn.college{EDs-BVSG2lvD78YkTAPDo_Zem0v.QX4ETO0wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
In this challenge, the main idea was to take the outputs of multiple commands and pipe them all together into a single command. 
I realized that instead of chaining every command with pipes directly, I could just put all the commands inside a shell script and 
then use that script’s output as one big input stream. So I opened nano and created a script named script.sh, where I wrote the 
two commands /challenge/pwn and /challenge/college. Once that was saved, I ran it using bash script.sh to make sure both commands executed 
properly. After confirming that, I took the next step — I piped the output of this script into /challenge/solve like this:
bash script.sh | /challenge/solve
This way, whatever both commands printed inside the script got combined and sent as input to /challenge/solve, and that’s how I 
finally got my flag.

```bash
~$ nano y.sh
hacker@chaining~redirecting-script-output:~$ bash y.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{EDs-BVSG2lvD78YkTAPDo_Zem0v.QX4ETO0wiN5gjNzEzW}
```
