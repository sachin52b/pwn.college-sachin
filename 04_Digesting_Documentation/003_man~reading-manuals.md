# Man~reading-manuals:
The challenge expected us to read the manual for challenge cmd and learn from reading the manual how to get the flag

## My solve
**Flag:** ` pwn.college{YzpNO8k4Mqrn0k07XV7LgcTKs26.QX0EDO0wiN5gjNzEzW}`

### Thought process
The task was to just write man cmd for challenge so that the manual opens, the manual opened and it had the instructions on how to get the 
flag(it was by using a particular argument with its argument being a certain number).
Next I just press q and invoked the /challenge/challenge command with the necessary arguments.

```bash
~$  /challenge/challenge --zpkqrn 840
Correct usage! Your flag: pwn.college{YzpNO8k4Mqrn0k07XV7LgcTKs26.QX0EDO0wiN5gjNzEzW}```
