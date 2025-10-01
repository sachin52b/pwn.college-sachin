# Process-exit-codes
The challenge’s purpose was to make us learn how to get the exit codes of a process or a command.

**Flag:** ` pwn.college{AlVss2XOdjzUlSX3J4LqnYfSlW0.QX5YDO1wiN5gjNzEzW} `

### Thought Process/Steps
The steps were simple and straightforward. The question mentioned that I had to get the exit code of a particular command. 
For that, I first invoked the command and then retrieved its exit code using echo $?. After this, I had to invoke another command 
using the exit code of the previous command as an argument (the exit code could be 0 for success or 1/another number for an error), 
which finally gave me the flag.

```bash
~$  /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
235
hacker@processes~process-exit-codes:~$ /challenge/submit-code 235
CORRECT! Here is your flag:
pwn.college{AlVss2XOdjzUlSX3J4LqnYfSlW0.QX5YDO1wiN5gjNzEzW}```
