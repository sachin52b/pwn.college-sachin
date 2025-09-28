# Multi-word-variables
The challenge’s purpose was to make us learn how to assign a particular  value of the variable.

## My solve
**Flag:** `  pwn.college{kDYgFX2e7Gx8qkhME3yXQqbgq3D.QXwYTN0wiN5gjNzEzW} `

### Thought process/Steps
I had to assign a full value(that had space in middle) to a particular variable but the tricky part was that I cannot use a space 
directly so for the full value I had to use “ ” in order to assign the value to the variable without any problems.

 ```bash
~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{kDYgFX2e7Gx8qkhME3yXQqbgq3D.QXwYTN0wiN5gjNzEzW} ```
