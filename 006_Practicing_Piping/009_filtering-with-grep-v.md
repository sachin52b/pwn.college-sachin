# Filtering-with-grep-v:
The challenge wanted us to ignore the decoy lines so the real flag stands out.
Its purpose was to teach using inverse filtering to remove undesired lines  and find the one correct result among many.

## My solve
**Flag:** `  pwn.college{0R4TfwOwpEdNvUlvf1N3_cqpKCQ.0FOxEzNxwiN5gjNzEzW}`

### Thought process/Steps
In the challenge, I redirected the output of /challenge/run into grep -v using a pipe (|). The main point was using grep -v, 
which lets us filter out lines containing a string we don’t want (in this case, DECOY). All the fake flags had DECOY in them, 
leaving only the real flag.

 ```bash
~$ /challenge/run | grep -v DECOY
pwn.college{0R4TfwOwpEdNvUlvf1N3_cqpKCQ.0FOxEzNxwiN5gjNzEzW}```
