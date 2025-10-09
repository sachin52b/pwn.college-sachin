# SCRIPTING-WITH-DEFAULT-CASES
The challenge’s purpose was to make us understand how to write a basic conditional statement in a shell script but this time there 
was an addition of else.

## MY SOLVE
**Flag:** ` pwn.college{UXs5Bl33tsSgh_MWDkgmsR6NTu2.01NzMDOxwiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
In this challenge I had to make a shell script (the usual business) and write a conditional statement in it such that if we input 
pwn as an argument we get college as the output but if we input something except college the output would be nope. Ok so firstly it 
was clear that if input is pwn then output is college for this much part if was enough but now what to do with the second thing 
that input something else then output is nope here came the work of info that was given in the challenge decription the else command 
we could simply append our code with else to get the desired output . once I saved my .sh file I gave it 2 arguments to check 
whether it was wrking fine further I ran /challenge/run to get my flag. Contents of my .sh file were:
```if [ "$1" == "pwn" ]
then
    echo "college"
else
       echo "nope"
fi
````

```bash
~$ bash ./solve.sh pwn
college
hacker@chaining~scripting-with-default-cases:~$ bash ./solve.sh blahblah
nope
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{UXs5Bl33tsSgh_MWDkgmsR6NTu2.01NzMDOxwiN5gjNzEzW}
```
