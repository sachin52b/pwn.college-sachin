
# Writing-to-multiple-programs
This challenge illustrates how process substitution can make commands act like files that accept input, allowing the output of 
one program to be sent simultaneously to multiple commands. It highlights a clever way to duplicate and redirect data streams 
in a single step, showing how helpful shell pipelines can become when combining tee with process substitution.

## My solve
**Flag:** `  pwn.college{gXKOu_NRlbNdmRMy0pNx30HnNFX.QXwgDN1wiN5gjNzEzW}`

### Thought process/Steps
In this challenge, I used process substitution to copy the output of one command into the input of multiple commands. 
We know that tee is normally used to copy a command’s stdout into files. Here, those “files” are created through 
process substitution (using >(cmd)), so we can use >(cmd) in place of a file. The data written to this “file” is actually sent as 
input to the command.

 ```bash
~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
1404569021286211960
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{gXKOu_NRlbNdmRMy0pNx30HnNFX.QXwgDN1wiN5gjNzEzW}```

