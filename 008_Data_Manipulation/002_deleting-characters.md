# Deleting-characters
The challenge’s purpose was to make us learn how to use tr for deleting letters( from a standard input to tr.

## My solve
**Flag:** ` pwn.college{csP8SAYrzNQ1l82x9IepI8WG_H8.0FNxEzNxwiN5gjNzEzW}`

### Thought process/Steps
The steps were basic and straight forward first I used | to convert the standard output of /challenge/run cmd to standard input 
for tr then I used (tr –d characters) to delete the characters mentioned in the question and get the correct flag.

 ```bash
~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{csP8SAYrzNQ1l82x9IepI8WG_H8.0FNxEzNxwiN5gjNzEzW}```
