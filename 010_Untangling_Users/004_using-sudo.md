# Using-sudo
The challenge’s purpose was to mainly  make us learn the use of  sudo cmd which is more widely used than su and is a much more 
modern approach.

**Flag:** ` pwn.college{sJcGw9Dn8TPoZwAUM5kAWdmZgDR.QX4UDN1wiN5gjNzEzW} `

### Thought Process/Steps
The challenge made the difference between su and sudo clear, and that helped shape my approach. I understood that su requires the 
password of the account you want to switch into, while sudo runs a single command with elevated privileges according to the system’s 
sudo rules (you don’t directly become that user—you just run one command as them). Since the flag was in /flag and needed root to 
read, I thought that running the read command through sudo would do the job. So I used sudo cat /flag to read the file as root and 
retrieve the flag.

```bash
~$ sudo cat /flag
pwn.college{sJcGw9Dn8TPoZwAUM5kAWdmZgDR.QX4UDN1wiN5gjNzEzW}```
