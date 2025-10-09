# READING-SHELL-SCRIPTS
The challenge’s purpose was to make us understand the importance of reading a script and how to do the same.

## MY SOLVE
**Flag:** ` pwn.college{0s1N_hf5bx7b0iDu3vx7OuIUSEq.0lMwgDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS

I had to read a shell script for this challenge, which felt odd — until now I’d only been creating scripts. Reading it was just 
like reading any file: I used the cat command on /challenge/run. The script contained:
```#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
    echo "CORRECT! Your flag:"
    cat /flag
else
    echo "Read the /challenge/run file to figure out the correct password!"
fi
```
I went through it line by line to understand what was happening. The challenge description hinted that the passcode could be found 
by reading the file — which turned out to simply mean examining how the script reads input (the read command). From the script I 
realized that when I run it, it prompts me to enter a value for GUESS. The if statement made the rest obvious: if I input hack the PLANET 
as the guess, the script prints the flag.

```bash
~$ cat /challenge/run
#!/opt/pwn.college/bash
read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{0s1N_hf5bx7b0iDu3vx7OuIUSEq.0lMwgDOxwiN5gjNzEzW}
```
