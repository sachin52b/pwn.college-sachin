# HANDLING-FAILURE
The main goal of the challenge was to make us learn how to chain commands with use of ||.

## MY SOLVE
**Flag:** `  pwn.college{4xrl_ZKl8s8jq7_gxRpW5hneMAl.01M0MDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
The thing here was using || (logical OR), which only runs the second command if the first one fails. To be sure the first binary 
actually failed, I ran /challenge/first-failure and then checked its exit status with echo $? — it printed 1, so I knew it 
returned a non-zero (error) code. Following the challenge instructions I chained the two commands with ||, so because the first 
command failed the shell ran the second one and I got the flag.

```bash
/challenge/first-failure
hacker@chaining~handling-failure:~$ echo $?
1
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{4xrl_ZKl8s8jq7_gxRpW5hneMAl.01M0MDOxwiN5gjNzEzW}
```
