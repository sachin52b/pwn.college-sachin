# Named pipes
The challenge made me learn about FIFO, how to create a FIFO and what are the differences in a FIFO and a normal file, 
the main purpose of  the challenge was to understand the blocking feature of FIFO. 

## My solve
**Flag:** `  pwn.college{Y7l2YJj_EobFl2O18aencDljlF5.01MzMDOxwiN5gjNzEzW} `

### Thought process/Steps
In this challenge, I had to redirect the output of a cmd(that output was basically the flag) into a fifo, this was done in the 
1st  terminal then I used cat cmd with the same fifo in another window(2nd terminal) to read the flag.


 ```bash
#TERMINAL 1
~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run  > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!
Bash will now try to open the FIFO for writing, to pass it as the stdout of
/challenge/run. Recall that operations on FIFOs will *block* until both the
read side and the write side is open, so /challenge/run will not actually be
launched until you start reading from the FIFO!
#TERMINAL 2
~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at
/tmp/flag_fifo! Here is your flag:
pwn.college{Y7l2YJj_EobFl2O18aencDljlF5.01MzMDOxwiN5gjNzEzW}```
