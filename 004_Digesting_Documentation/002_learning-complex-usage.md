# Learning-complex-usage

The challenge expected us to learn that maybe some more complex commands in which we can give argument to the argument. 
A similar case was provided as the challenge where we had to give the path of flag file as an argument to an argument to 
get our flag.

## My solve
**Flag:** `pwn.college{sV5uC4R-kBNfeh0vxZtcyivNSUV.QX1ITO0wiN5gjNzEzW}`

### Thought process
The task was simple and straightforward. The documentation had already specified which argument to use when invoking the command. 
What remained was providing an argument to that argument, which in this case was the path of the flag file. 
Therefore, /flag became the argument for --printfile.


```bash
~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{sV5uC4R-kBNfeh0vxZtcyivNSUV.QX1ITO0wiN5gjNzEzW}```
