# TWEAKING-PRACTICE
The main goal of the challenge was to make us practice chmod.

## MY SOLVE
**Flag:** ` pwn.college{0FrhsT4kputG_4Rm72JSSJZkNCx.QXwEjN0wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
This challenge was basically a chmod practice. I had to go through eight rounds of changing the permission mode on /challenge/pwn 
so the challenge itself would change the ownership of /flag for me. After those rounds finished, I still needed to 
adjust /flag’s mode so the hacker user could read it — once I gave the read bit to the right class, I ran cat /flag and got the flag. 
Surprisingly, I didn’t mistype any commands: every chmod argument I used worked on the first try.

Below I am pasting the cmds I used according to instructions that were given

```bash
chmod o+x /challenge/pwn
chmod go+w /challenge/pwn
chmod u+x /challenge/pwn
chmod go-rw /challenge/pwn
chmod u-rwx /challenge/pwn
chmod o+rw /challenge/pwn
chmod o-rx /challenge/pwn
chmod uo+rw /challenge/pwn
~$ chmod uo+rw /challenge/pwn
You set the correct permissions!
You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!
~$ chmod u+r /flag
hacker@permissions~permission-tweaking-practice:~$ ls -l /flag
-r-------- 1 hacker hacker 60 Oct  7 09:45 /flag
hacker@permissions~permission-tweaking-practice:~$ cat /flag
pwn.college{0FrhsT4kputG_4Rm72JSSJZkNCx.QXwEjN0wiN5gjNzEzW}
```

