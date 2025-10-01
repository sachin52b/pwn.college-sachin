# Deleting-newlines
The challenge’s purpose was to make us learn how to use tr for deleting newlines( from a standard input to tr).

## My solve
**Flag:** ` pwn.college{kyQDwFIJu-uONzJ0lYC0FrlA447.0VNxEzNxwiN5gjNzEzW}`

### Thought process/Steps
The steps were basic and straight forward first I used | to convert the standard output of /challenge/run cmd to standard input 
for tr then I used (tr –d  “\n”) to delete the new lines and get the correct flag.

 ```bash
~$ /challenge/run | tr –d "\n"
Your line-split flag: pwn.college{kyQDwFIJu-uONzJ0lYC0FrlA447.0VNxEzNxwiN5gjNzEzW} ```
