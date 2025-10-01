# Grepping-live-output
The challenge wanted us to learn how to send one program’s output straight into another so you don’t have to save it to a file first.
Its goal was to show how to handle big outputs on the fly and quickly find the flag without creating temporary file i.e 
basically  done through piping.

## My solve
**Flag:** `  pwn.college{kj-gmJrPUAM7fWdC7M2Vvqbijbp.QX5EDO0wiN5gjNzEzW}`

### Thought process/Steps
In the challenge, I had to redirect the output of the command /challenge/run into the input of other command directly which I 
performed by using |. 

 ```bash
~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{kj-gmJrPUAM7fWdC7M2Vvqbijbp.QX5EDO0wiN5gjNzEzW}```
