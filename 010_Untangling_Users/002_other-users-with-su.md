# Other-users-with-su
The challenge’s purpose was to make us learn how to switch to some other user using the su cmd.

**Flag:** ` pwn.college{8huvJhtEMt1c4X_vqeW-DtMbQYe.QX2UDN1wiN5gjNzEzW} `

### Thought Process/Steps
This challenge felt like a small variation of the previous one. Earlier, I had seen that using su without any arguments switches 
the user to root after providing the correct password. From that hint, I realized that if I wanted to switch to another user, I 
could simply specify the username after su. Since the question explicitly asked me to switch to the user zardus, I tried running 
su zardus (the format was already shown in the examples). The password was given in the challenge, so I entered it, and just like 
that, I was logged in as zardus. After that, all I needed to do was run /challenge/run, which finally gave me the flag.

```bash
~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{8huvJhtEMt1c4X_vqeW-DtMbQYe.QX2UDN1wiN5gjNzEzW}```
