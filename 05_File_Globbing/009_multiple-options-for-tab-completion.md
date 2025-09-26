# Multiple-options-for-tab-completion
The challenge’s purpose was to multiple options with the tab-completion feature like what happens with a single press of tab

## My solve
**Flag:** ` pwn.college{8r4rEjF0kdcmg6dkiHCDTvGeme4.0lN0EzNxwiN5gjNzEzW}`

### Thought process/Steps
The steps were straightforward. I had to use the cat command on a particular file, but I couldn’t type its full name directly 
(this was the constraint). So, I used the Tab key for automatic completion. Since there were multiple files with the same initial letters, 
the first press of Tab completed the name only up to the point that was common to all matching files. Pressing Tab a second time displayed 
a list of all files with those initials, from which I could identify which file contained the flag.

 ```bash
~$ cat /challenge/files/pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-f
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-f
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-f
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{8r4rEjF0kdcmg6dkiHCDTvGeme4.0lN0EzNxwiN5gjNzEzW} ```
