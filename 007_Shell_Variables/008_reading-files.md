# Reading-files
The challenge’s purpose was to make us learn how to take a file as the standard input of read command so that the file content is directly 
stored in the variable in a single compact command.

## My solve
**Flag:** ` pwn.college{UYOrm3Zao-h_qp38dJLN_qE9hSb.QXwIDO0wiN5gjNzEzW}`

### Thought process/Steps
The steps were basic and straightforward, I used read and command input < directly to achieve the flag—
read var_name < file_name.


 ```bash
~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{UYOrm3Zao-h_qp38dJLN_qE9hSb.QXwIDO0wiN5gjNzEzW}```
