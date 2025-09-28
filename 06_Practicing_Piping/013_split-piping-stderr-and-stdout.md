# Split-piping-stderr-and-stdout
The challenge expected us to write the sted err and std out of a particular command to two diff separate commands, the 
challenge basically expected us to figure out a way from previous challenges to do the same.

## My solve
**Flag:** `  pwn.college{IUZSQUe_ws-pxwF3YDQJl-xe5fU.QXxQDM2wiN5gjNzEzW}`

### Thought process/Steps
In this challenge, I used process substitution to redirect the standard output of one command into the input of another command, 
and to redirect the standard error of the same command to a different command. I first used > and 2> to redirect output and error, 
but those send the data to files then the use of Process substitution allowed me to redirect them further to the desired commands 
instead.

 ```bash
~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{IUZSQUe_ws-pxwF3YDQJl-xe5fU.QXxQDM2wiN5gjNzEzW}```
