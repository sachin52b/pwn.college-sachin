# SCRIPTING-WITH-ARGUMENTS
The challenge’s purpose was to make us understand how to make shell scripts take arguments.

## MY SOLVE
**Flag:** `  pwn.college{MiC3ZI_WGB515PCGq9rMTwseksW.0VNzMDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
The challenge had already explained how a script can take arguments. Instead of hardcoding the arguments in the 
commands inside the script, I could use $1, $2, $3, and so on, corresponding to the number of arguments, and then 
provide the real arguments when running the script.
For this particular challenge, I created a shell script using nano, and wrote echo $2 $1 in it, as the challenge 
required the second argument to be printed first. I saved the file, and then ran the script using bash, providing 
the actual arguments to get the desired output. Finally, /challenge/run verified everything and gave me the flag.

```bash
~$ nano solve.sh
hacker@chaining~scripting-with-arguments:~$ bash ./solve.sh pwn college
college pwn
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{MiC3ZI_WGB515PCGq9rMTwseksW.0VNzMDOxwiN5gjNzEzW}
```
