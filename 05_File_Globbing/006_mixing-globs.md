# Mixing globs
The challenge’s purpose was to learn how to use different globs together to access exactly the desired files.

## My solve
**Flag:** ` pwn.college{kwsaJ0UmQKY49OZXyYhoFcnab84.QX1IDO0wiN5gjNzEzW}`

### Thought process/Steps
First, I used the cd command to go into /challenge/files. Then I ran /challenge/run with a six-letter argument so that files named 
challenging, pwning, and educational would be matched. To target those specific names I combined a character class [...] with a wildcard *. 
I was basically experimenting with different glob patterns until I found a combination that matched the required files.

 ```bash
/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{kwsaJ0UmQKY49OZXyYhoFcnab84.QX1IDO0wiN5gjNzEzW}```
