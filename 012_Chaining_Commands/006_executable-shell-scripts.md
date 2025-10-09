# EXECUTABLE-SHELL-SCRIPTS
The challenge main purpose was to tell us a way we can avoid use of bash for running our shell scripts.

## MY SOLVE
**Flag:** `  pwn.college{oH80F9PQOM1_dIXycWDKqhzhMWP.QX0cjM1wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
The main idea of this challenge was to stop calling bash every time I wanted to run my shell script. The description pointed out 
another way: once the script exists and the commands are written inside it, you don’t need to run it with bash — you can just make 
the file executable and run it directly. That raised the obvious question: how do you make it executable? I remembered from the 
previous module that chmod is how you change file permissions, so I used it to give execute permission to the owner:
chmod u+x z.sh
After that I ran the script from my current working directory (the prompt even hinted at the exact form). The script executed, did what it 
was supposed to, and I got the flag.

```bash
:~$ nano z.sh
hacker@chaining~executable-shell-scripts:~$ chmod u+x z.sh
./z.sh
Congratulations on your shell script execution! Your flag:
pwn.college{oH80F9PQOM1_dIXycWDKqhzhMWP.QX0cjM1wiN5gjNzEzW}```

