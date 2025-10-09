# SCRIPTING-WITH-MULTIPLE-CONDITIONS
The challenge’s purpose was to make us understand how to write a syntax that takes in account multiple conditions. It’s goal was 
to make us teach combined use of if,elif,else.

## MY SOLVE
**Flag:** ` pwn.college{AfUZZ1sX7xsYGwyF9ehQMmrTVY7.0FOzMDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
This challenge made me think a bit about how shell scripts choose between many possible inputs — I read the requirements and 
realized right away that a single if (or if/else) wouldn’t cover four different outputs, so I needed elif branches to check each 
case in order. I created a script and walked through the logic in my head: “if $1 is hack print the planet; otherwise check if 
it’s pwn and print college; otherwise check learn and print linux; otherwise fall back to unknown.” While coding I was careful to 
keep the exact spacing and quotes the shell expects (that subtlety about [ and ] matters), then I saved the file and tested it by 
running the script with different arguments to make sure each branch executed as intended. Satisfied it worked, I invoked 
/challenge/run and got the flag.

Contents of my .sh file:

```if [ "$1" == "hack" ]
then
    echo "the planet"
elif [ "$1" == "pwn" ]
then
    echo "college"
elif [ "$1" == "learn" ]
then
    echo "linux"
else
    echo "unknown"
fi
```

```bash
~$ nano solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$  bash ./solve.sh hack
the planet
hacker@chaining~scripting-with-multiple-conditions:~$  bash ./solve.sh pwn
college
hacker@chaining~scripting-with-multiple-conditions:~$  bash ./solve.sh linux
unknown
hacker@chaining~scripting-with-multiple-conditions:~$  bash ./solve.sh learn
linux
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{AfUZZ1sX7xsYGwyF9ehQMmrTVY7.0FOzMDOxwiN5gjNzEzW}```
