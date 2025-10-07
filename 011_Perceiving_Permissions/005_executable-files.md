# EXECUTABLE-FILES
The challenge expected to us to learn and implement how to change the permissions user/group/other has to the file i.e mainly the 
use of chmod command. The challenge specifically required us to make a file executable.

## MY SOLVE
**Flag:** ` pwn.college{Ux-PEjKV7L2TwByxdbNfLo4c0cA.QXyEjN0wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
I needed to make /challenge/run executable so I could get the flag. I started by checking ownership and permissions with 
ls -l /challenge/run. The output showed the file was owned by me (hacker) but the mode was -r--r--r-- — readable by everyone, 
but no execute bits set. That told me I didn’t need to change the owner or group; since I’m the owner, the fix was to add the 
owner’s execute bit. I ran chmod u+x /challenge/run to grant execute permission to the user, double checked the mode with ls -l 
to make sure the change took, and then executed /challenge/run to retrieve the flag.

```bash
~$ ls -l /challenge/run
-r--r--r-- 1 hacker hacker 32 Jan 14  2025 /challenge/run
hacker@permissions~executable-files:~$ chmod u+x /challenge/run
hacker@permissions~executable-files:~$ ls -l /challenge/run
-r-xr--r-- 1 hacker hacker 32 Jan 14  2025 /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{Ux-PEjKV7L2TwByxdbNfLo4c0cA.QXyEjN0wiN5gjNzEzW}
```

