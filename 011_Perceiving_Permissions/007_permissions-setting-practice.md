# PERMISSIONS-SETTING-PRACTICE
The main goal of the challenge was to make us do more practice of chmod that include both modifying as well as setting/overwriting 
permissions.

## MY SOLVE
**Flag:** ` pwn.college{8d_O_EFQB7F7UPrDFhxyPQBPT5W.QXzETO0wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
This challenge was basically a chmod practice. This time we were told in the challenge that we could set completely new permissions 
or override the previous by using ‘=’ .I had to go through eight rounds of changing the permission mode on /challenge/pwn so the 
challenge itself change the ownership of /flag for me. After those rounds finished, I still needed to adjust /flag’s mode so the 
hacker user could read it — once I gave the read bit to the right class, I ran cat /flag and got the flag. Surprisingly, I didn’t 
mistype any commands: every chmod argument I used worked on the first try. It all started by me invoking /challenge/run to start 
off the challenge.
Round by  Round Description: 
Round 1
chmod u=-,g+w,o=- /challenge/pwn
I saw rw-r--r-- and needed ---rw---- — so owner and others must be cleared and group given write. I set each class explicitly (u=-) 
to avoid leaving stray bits; confirmed it became ---rw----.
Round 2
chmod g-w,o=rx /challenge/pwn
From ---rw---- the goal was ---r--r-x: remove group write and make others rx. I removed the group write and explicitly set others 
to rx so no accidental write bit remained.
Round 3
chmod u=rwx,o=w /challenge/pwn
Target rwxr---w- meant owner needed full rwx and others only w. I assigned owner exactly rwx and others w to preserve group read.
Round 4
chmod u-wx,g+wx,o+x /challenge/pwn
Going from rwxr---w- to r--rwx-wx meant removing owner write+exec, giving group wx, and adding exec for others. I removed the two 
owner bits and added the group/other bits incrementally.
Round 5
chmod u=wx,g=x,o=- /challenge/pwn
Needed -wx--x---: owner wx, group x, no others. I set owner and group precisely and cleared others with o=- so nothing unexpected 
stayed set.
Round 6
chmod u-x,g+rw,o=rx /challenge/pwn
From -wx--x--- to -w-rwxr-x I removed the owner exec, promoted group to rw, and made others rx. Minimal changes kept owner as w 
while building group/other bits.
Round 7
chmod u=rx,g-wx,o=wx /challenge/pwn
Target r-xr---wx required owner rx, group read only, others wx. I set owner exactly, stripped group write+exec, and gave others 
write+exec.
Round 8
chmod u=w,g+w,o=r /challenge/pwn
Final goal -w-rw-r-- meant owner w, group rw, others r. I set owner and others explicitly and added group write to turn its existing read into rw.
Below I am pasting the cmds I used according to instructions that were given
```bash
chmod u=-,g+w,o=- /challenge/pwn
chmod g-w,o=rx /challenge/pwn
chmod u=rwx,o=w /challenge/pwn
chmod u-wx,g+wx,o+x /challenge/pwn
chmod u=wx,g=x,o=- /challenge/pwn
chmod u-x,g+rw,o=rx /challenge/pwn
chmod u=rx,g-wx,o=wx /challenge/pwn
chmod u=w,g+w,o=r /challenge/pwn
~$ chmod u=w,g+w,o=r /challenge/pwn
You set the correct permissions!
You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!
~$ ls -l /flag
---------- 1 hacker hacker 60 Oct  7 10:18 /flag
hacker@permissions~permissions-setting-practice:~$ chmod u+r /flag
hacker@permissions~permissions-setting-practice:~$ cat /flag
pwn.college{8d_O_EFQB7F7UPrDFhxyPQBPT5W.QXzETO0wiN5gjNzEzW}
```
