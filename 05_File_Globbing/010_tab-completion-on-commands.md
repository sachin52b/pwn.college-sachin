
# Tab-completion-on-commands
The challenge’s purpose was explore how tab completion work with commands.

## My solve
**Flag:** ` pwn.college{IHamnS0Fldyn4bZ8xvZ2UxIea3Z.0VN0EzNxwiN5gjNzEzW}`

### Thought process/Steps
The steps were straightforward. I had to invoke a command that started with pwncollege, but I didn’t know the full command, so I pressed Tab.
The shell’s auto‑completion feature finished the command for me, and I was then able to run it to get the flag.

 ```bash
~$ pwncollege-27571
Correct! Here is your flag:
pwn.college{IHamnS0Fldyn4bZ8xvZ2UxIea3Z.0VN0EzNxwiN5gjNzEzW}```
