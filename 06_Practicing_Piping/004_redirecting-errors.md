# Redirecting-errors
The challenge wanted us to practice sending normal output and error messages into different files. 
The goal was to help us understand how file descriptors work and how to use them to separate outputs in Linux.

## My solve
**Flag:** `  pwn.college{YWBZwae-yTQ3sqOZs6gS_4GKCkl.QX3YTN0wiN5gjNzEzW}`

### Thought process/Steps
The steps were straightforward. I redirected the output of /challenge/run (which outputs the flag) into a file using > ,  
using 2> I also redirected the standard error to another file.Finally, I displayed the flag & instructions  with cat and the filenames as the arguments.

 ```bash
~$ /challenge/run > myflag 2> instructions
~$ cat myflag instructions

[FLAG] Here is your flag:
[FLAG] pwn.college{YWBZwae-yTQ3sqOZs6gS_4GKCkl.QX3YTN0wiN5gjNzEzW}

[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements..```
