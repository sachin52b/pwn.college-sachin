# Duplicating-piped-data-with-tee
The main purpose of teaching was to  how to grab and look at the data flowing between commands while still passing it along.This helps 
you save a copy of the middle output and see what a later command expects, which makes debugging much easier.

## My solve
**Flag:** `  pwn.college{w_g0mTtFpwdwsGpmCYx_ZmtJ8Aa.QXxITO0wiN5gjNzEzW}`

### Thought process/Steps
In this challenge, I had to pipe the output of /challenge/pwn to /challenge/college, but there was a twist: the default output 
of /challenge/pwn was not a proper input for /challenge/college. I first used tee to capture the output of /challenge/pwn — in this 
case, a usage hint — so I could see what it required. Then, using the information from the hint, I ran /challenge/pwn with the 
correct input and piped the proper output into /challenge/college, which gave me the flag

 ```bash
:~$ /challenge/pwn | tee cmd1_output | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat cmd1_output
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "w_g0mTtF"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret w_g0mTtF | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{w_g0mTtFpwdwsGpmCYx_ZmtJ8Aa.QXxITO0wiN5gjNzEzW}```
