# BUILDING-ON-SUCCESS
The main goal of the challenge was to make us learn how to chain commands with use of &&.

## MY SOLVE
**Flag:** `  pwn.college{oIyRMP4Npilkly_8yTsOmPfRzQk.0lM0MDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
I had to chain two commands using &&, so my thinking was all about conditional execution: cmd1 && cmd2 runs the second command only 
if the first one succeeds (i.e., exits with status 0); if the first command fails (non-zero exit), the second command is skipped.
In the challenge the prompt required that exact behavior — the first program had to finish successfully before the second one could run 
and produce the flag — so I wrote the commands like: /first/command && /second/command
I picked && deliberately because it guarantees the second step only happens when the first step worked, which matches the challenge’s 
requirement that success of step one is a precondition for step two (and ultimately for getting the flag). But also before using && I executed the cmds separately and as mentioned in the description I didn’t get the flag.

```bash
~$ /challenge/first-success
hacker@chaining~building-on-success:~$ /challenge/second
Error: /challenge/first-success must be successfully chained with
/challenge/second using &&
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second
Nice chaining! Flag: pwn.college{oIyRMP4Npilkly_8yTsOmPfRzQk.0lM0MDOxwiN5gjNzEzW}
```


