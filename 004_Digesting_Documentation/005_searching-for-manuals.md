# Searching-for-manuals
The challenge required first searching the man page for “challenge,” since its name had been changed. After locating this hidden 
man page, reading it provided the argument needed to print the flag, which ultimately revealed the flag itself.

## My solve
**Flag:** ` pwn.college{8uoi0-MeD_ni21yAgkKKvJdFAih.QX2EDO0wiN5gjNzEzW}`

### Thought process/Steps
The steps were basically as follows: first, I used man man to understand how the man command works and learn about the arguments 
it accepts. From there, I learned about the man -k "keyword" command, which helped me locate the man page for the challenge,
even though it had been renamed. Finally, I used man on that page to find the argument needed to retrieve the flag, and by using it, 
I was able to get the flag.


```bash
~$ man man
hacker@man~searching-for-manuals:~$ man -key challenge
uoieniygkv (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man uoieniygkv
hacker@man~searching-for-manuals:~$ /challenge/challenge --uoieni 802
Correct usage! Your flag: pwn.college{8uoi0-MeD_ni21yAgkKKvJdFAih.QX2EDO0wiN5gjNzEzW}```

