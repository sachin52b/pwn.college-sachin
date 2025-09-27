
# Piping~redirecting-more-output
The challenge’s purpose was  to learn redirecting standard output to files which can be accomplished by the the > character.

## My solve
**Flag:** ` pwn.college{UmMmWPeQwTJ9gk6r_d5GkYGmBeP.QX1YTN0wiN5gjNzEzW}`

### Thought process/Steps
The steps were straightforward. I had to redirect the output of /challenge/run (which outputs the flag) into a file using >. Then, 
to display the flag, I used the cat command with that file as the argument.

 ```bash
~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{UmMmWPeQwTJ9gk6r_d5GkYGmBeP.QX1YTN0wiN5gjNzEzW}```
