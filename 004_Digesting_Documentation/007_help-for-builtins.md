# Help-for-builtins
The challenge was so that the usage  of help can be understood. help was to be used to get the info about the arguments of the 
built –in commands. 

## My solve
**Flag:** ` pwn.college{AetZ71URlcMVlSoDxRNF-YPXho_.QX0ETO0wiN5gjNzEzW}`

### Thought process/Steps
The steps were straightforward, I used help to get the command’s documentation. There was an argument which allowed us to get the flag by 
using another argument with it that was also mentioned in the documentation.

```bash
~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "AetZ71UR".
hacker@man~help-for-builtins:~$ challenge --secret AetZ71UR
Correct! Here is your flag!
pwn.college{AetZ71URlcMVlSoDxRNF-YPXho_.QX0ETO0wiN5gjNzEzW}```
