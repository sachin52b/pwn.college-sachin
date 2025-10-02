# Becoming-root-with-su
The challenge’s purpose was to make us learn how to become the root using the substitute user command su.

**Flag:** ` pwn.college{I2FRxvP_Hm-mClV22PtqmfQZuIX.QX1UDN1wiN5gjNzEzW} `

### Thought Process/Steps
In the challenge, it was explained that the su command is used to switch users, and in older times it was commonly used to become 
the root user by providing the correct password. This gave me the idea to try using su myself. When I typed the command, the 
terminal asked me for a password. Since the question had already provided one, I entered it, and as expected, I was switched to 
the root account. Once I had root access, the next step was to retrieve the flag. From my experience in previous challenges, I 
knew that the flag is usually stored in the /flag file, so I simply ran cat /flag and was able to read the flag successfully.

```bash
~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{I2FRxvP_Hm-mClV22PtqmfQZuIX.QX1UDN1wiN5gjNzEzW}```
