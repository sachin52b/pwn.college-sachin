# Printing-exported-variables
The challenge’s purpose was to make us learn how to print set of exported variables.

## My solve
**Flag:** ` pwn.college{ITe6BJeXBZI5RoBJR_3x0dl9Coa.QX4UTN0wiN5gjNzEzW}`

### Thought process/Steps
I just invoked env command and then looked at the list of exported variables to find the flag.

 ```bash
~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=6a89d5800059e39c770bbddff8ca4193d36d19b99204bb334c1b5cfdd135b855
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{ITe6BJeXBZI5RoBJR_3x0dl9Coa.QX4UTN0wiN5gjNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env```
