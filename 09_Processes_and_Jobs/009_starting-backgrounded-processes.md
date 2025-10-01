# Starting-backgrounded-processes
The challenge’s purpose was to make us learn how to directly background a process(making it run in the background) in 
a single step.

**Flag:** ` pwn.college{4K6cjc2zXlTK5FaT0pHamycmjIu.QX5QDO0wiN5gjNzEzW}`

### Thought Process/Steps
The steps were simple and straightforward. The question mentioned that, instead of doing multiple steps—running /challenge/run,
suspending it with CTRL+Z (which pauses the process in a stopped background state), and then resuming it in the background 
with bg—I could have simply started the process in the background directly by adding & at the end of the command when 
first launching it 

```bash
~$ /challenge/run &
[1] 138
hacker@processes~starting-backgrounded-processes:~$


Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{4K6cjc2zXlTK5FaT0pHamycmjIu.QX5QDO0wiN5gjNzEzW}

[1]+  Done                    /challenge/run```
