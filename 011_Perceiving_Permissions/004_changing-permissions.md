
# CHANGING-PERMISSIONS
The challenge expected to us to learn and implement how to change the permissions user/group/other has to the file i.e mainly the 
use of chmod command.

## MY SOLVE
**Flag:** ` pwn.college{UBEDlkJJMuy64TvyBB30-MFN91I.QXzcjM1wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
There was a lot to read at the start — the challenge focused on chmod, but the actual goal was: make /flag readable by me 
(the hacker user). The first thing I thought was “check the current permissions,” so I ran ls -l. The output showed -r-------- 1 — 
in other words, only the owner (root) had read permission. That told me two things: root could already read the file, and I 
couldn’t, because I’m not root and I don’t belong to root’s group. Practically that means I fall into the “other” category, so I 
needed to give read permission to others.
Since the challenge itself taught the symbolic mode format, I used chmod o+r /flag (give read access to others). I ran ls -l again 
to confirm the change — the mode had updated to -r-----r-- — and then I simply ran cat /flag to read the flag. The whole process 
was driven by a simple chain of questions I kept asking myself: what do the bits say, which class am I in (owner/group/other), and 
which permission change will make the file readable to me?

```bash
~$ ls -l /flag
-r-------- 1 root root 60 Oct  7 09:12 /flag
hacker@permissions~changing-permissions:~$ chmod o+r /flag
hacker@permissions~changing-permissions:~$ ls -l /flag
-r-----r-- 1 root root 60 Oct  7 09:12 /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{UBEDlkJJMuy64TvyBB30-MFN91I.QXzcjM1wiN5gjNzEzW}
```
