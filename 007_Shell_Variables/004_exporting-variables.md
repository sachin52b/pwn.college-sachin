# Exporting-variables
The challenge’s purpose was to make us learn how to assign a particular  value to the variable and export at the same time so that
it could also be used in another shell.
## My solve
**Flag:** `  pwn.college{40dgkoKA72kNbFR3JAmhtE3sQ0e.QXyYTN0wiN5gjNzEzW}`

### Thought process/Steps
I used export var_name=value to create a variable and assign a value to it at the same time. The challenge also required creating a 
variable and assigning a value without exporting it. After completing both tasks, I simply invoked /challenge/run to get the flag

 ```bash
~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{40dgkoKA72kNbFR3JAmhtE3sQ0e.QXyYTN0wiN5gjNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!```
