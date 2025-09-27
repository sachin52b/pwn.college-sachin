
# Grepping-errors:
The challenge expected us to learn how to redirect file descriptors so that we can even print stderr through |(pipe).

## My solve
**Flag:** `  pwn.college{gkCtBPoX8KBzwHYviQ8vs8AI3SY.QX1ATO0wiN5gjNzEzW}`

### Thought process/Steps
In the challenge, I had to redirect one file descriptor to another (stderr to stdout) using >&. The main goal was to combine stderr 
and stdout because a pipe (|) only takes stdout. I then piped the combined stdout into grep with the search string pwn.college 
to get the flag


 ```bash
~$ /challenge/run 2>& 1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{gkCtBPoX8KBzwHYviQ8vs8AI3SY.QX1ATO0wiN5gjNzEzW}```

