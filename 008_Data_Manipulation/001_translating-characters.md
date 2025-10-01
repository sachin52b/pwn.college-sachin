# Translating-characters
The challenge’s purpose was to make us learn how to use tr for converting letters( from a standard input to tr) to any other 
desired letters.

## My solve
**Flag:** ` pwn.college{gOdjWPTbvElqW-GQ2NMp9SpqscE.01MxEzNxwiN5gjNzEzW}`

### Thought process/Steps
The steps were basic and straight forward first I used | to convert the standard output of /challenge/run cmd to standard input 
for tr then I gave arguments to the tr command to get the desired result.

 ```bash
~$ /challenge/run | tr ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
yOUR CASE-SWAPPED FLAG:
pwn.college{gOdjWPTbvElqW-GQ2NMp9SpqscE.01MxEzNxwiN5gjNzEzW}```
