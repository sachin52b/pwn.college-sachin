
# THE-SUID-BIT
The main goal of the challenge was to make us learn about SUID bit and how to add it to the mode.

## MY SOLVE
**Flag:** ` pwn.college{Q9i2k7YxBtajz9dDY9sSlPKbVNA.QXzEjN0wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
The challenge introduced SUID — that little s that replaces the owner’s x bit. I reminded myself what that means: if a program has 
the SUID bit set, it runs with the owner’s privileges (not the caller’s), so any user executing it effectively runs it as the 
owner. In this case /challenge/getroot was owned by root and, when run as root, spawns a root shell — but as hacker I couldn’t 
run it with root privileges unless I set the SUID bit myself.So I set the SUID bit with chmod u+s /challenge/getroot, then executed 
/challenge/getroot. A root shell popped up, and from there I ran cat /flag to read the flag

```bash
:~$ chmod u+s  /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root!
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{Q9i2k7YxBtajz9dDY9sSlPKbVNA.QXzEjN0wiN5gjNzEzW}
```
