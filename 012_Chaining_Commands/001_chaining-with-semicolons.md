# CHAINING-WITH-SEMICOLONS
The main goal of the challenge was to make us learn how to chain commands with use of ;.

## MY SOLVE
**Flag:** ` pwn.college{IvxNvM3vv_TYCDZpp0ToifxUdnY.QX1UDO0wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
The challenge wanted me to run two specific commands, /challenge/pwn and /challenge/college. I figured the simplest way was to 
write them one after the other with a semicolon: /challenge/pwn; /challenge/college I used ; because it just runs the first command, 
then runs the second.

```bash
~$ /challenge/pwn ; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{IvxNvM3vv_TYCDZpp0ToifxUdnY.QX1UDO0wiN5gjNzEzW}
```
