# Exclusionary-globbing
The challenge’s purpose was to learn exclusionary globbing.

## My solve
**Flag:** ` pwn.college{8Oia0kCWemmGFqMtBuzovs0qKes.QX2IDO0wiN5gjNzEzW}`

### Thought process/Steps
First, I used the cd command to go into /challenge/files. Then I ran /challenge/run with a 8-letter argument so that files except those starting 
with p,w,n are . To target those specific names I combined a character class [...] with a wildcard * — 
but this time in [] I had to use ^ for Exclusionary globbing.

 ```bash
/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{8Oia0kCWemmGFqMtBuzovs0qKes.QX2IDO0wiN5gjNzEzW}```
