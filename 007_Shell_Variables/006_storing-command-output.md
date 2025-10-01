# Storing-command-output:
The challenge’s purpose was to make us learn how to assign the output of a command directly into a variable.

## My solve
**Flag:** ` pwn.college{YhwBCMEADt7T6W6QExrQ8bncgiC.QX1cDN1wiN5gjNzEzW}`

### Thought process/Steps
I used the syntax var_name=$(cmd) to store the output of the cmd(which was actually the flag in this case) into my variable 
and then I used echo $var_name to print the flag.

 ```bash
~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{YhwBCMEADt7T6W6QExrQ8bncgiC.QX1cDN1wiN5gjNzEzW}```
