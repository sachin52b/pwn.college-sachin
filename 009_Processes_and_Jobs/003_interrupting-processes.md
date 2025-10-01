
# Interrupting-processes
The challenge’s purpose was to make us learn how to interrupt a process and make a clean exit

## My solve
**Flag:** ` pwn.college{knQS8XIFTY6HPloE4ZORUyfU-3R.QXzQDO0wiN5gjNzEzW} `

### Thought Process/Steps
The steps were simple and straightforward. The question mentioned that we had to run /challenge/run, but the twist was that 
we had to interrupt this process to get our flag. Interrupting it was easy — I just had to press Ctrl+C.

 ```bash
~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{knQS8XIFTY6HPloE4ZORUyfU-3R.QXzQDO0wiN5gjNzEzW}```
