
# Helpful-programs
The challenge was so that the usage  of --help can be understood. –help was to be used to get the info about the arguments of the cmd which 
would further help us to take out the flag. 


## My solve
**Flag:** ` pwn.college{cevAjEGfJ52BvjRuDBmJJusYpBQ.QX3IDO0wiN5gjNzEzW}`

### Thought process/Steps
The steps were as follows: I used --help to get the command’s documentation. The first argument allowed us to print a number, 
and this number then became the argument for a second option, which ultimately gave us the flag.


```bash
~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 523
hacker@man~helpful-programs:~$ /challenge/challenge -g 523
Correct usage! Your flag: pwn.college{cevAjEGfJ52BvjRuDBmJJusYpBQ.QX3IDO0wiN5gjNzEzW}```

