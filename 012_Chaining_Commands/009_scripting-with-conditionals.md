
# SCRIPTING-WITH-CONDITIONALS
The challenge’s purpose was to make us understand how to write a basic conditional statement in a shell script.

## MY SOLVE
**Flag:** `pwn.college{sKJG1E19FnVGJeYqY0aI_dnOjEp.0lNzMDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
This challenge felt fresh because I was meeting if for the first time in a shell script. The description warned there’s a very 
particular way to write the if — you must be careful with spaces and the exact syntax — so I read that part slowly and kept it in 
mind while coding. I created solve.sh and realized the task was simple: if the script is given pwn as the first argument it should 
print college, otherwise do nothing. So I wrote the condition exactly as required:
```
if [ "$1" == "pwn" ]
then
    echo "college"
fi
```
I saved the file, ran it with bash and the argument pwn, and it printed college, which told me the logic was correct. Finally I 
invoked /challenge/run and got the flag.

```bash
~$ nano solve.sh
hacker@chaining~scripting-with-conditionals:~$  bash ./solve.sh pwn
college
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{sKJG1E19FnVGJeYqY0aI_dnOjEp.0lNzMDOxwiN5gjNzEzW}
```
