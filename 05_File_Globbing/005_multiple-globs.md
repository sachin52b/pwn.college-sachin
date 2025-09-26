# Multiple-globs
The challenge’s purpose was to learn how to multiple globs.

## My solve
**Flag:** ` pwn.college{0ed2XKpSYFlVN9yTeP-GW9gGOKp.0lM3kjNxwiN5gjNzEzW}`

### Thought process/Steps
First, I used the cd command to go into /challenge/files. Then I invoked /challenge/run with an argument of only three letters so 
that files containing the letter p would be included. To match filenames where p appears anywhere (at the start, middle, or end) 
I used the glob *p* — the * allows any characters before and after p.

```bash
~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{0ed2XKpSYFlVN9yTeP-GW9gGOKp.0lM3kjNxwiN5gjNzEzW}```
