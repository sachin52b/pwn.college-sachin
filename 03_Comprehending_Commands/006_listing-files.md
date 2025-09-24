# Listing-files

This challenge expected us to find the flag by executed the desired file run .

## My solve
**Flag:** `pwn.college{ItWXkvtDKA9pjEi13CS8UR_Ph1j.QX4IDO0wiN5gjNzEzW}`

### Thought process
we were given a directory challenge i used ls command to list the files in it. A.T.Q the run file was named 
randomly after using ls command the renamed run file was found then i invoked /challenge/new_run_file to get the flag.




```bash
~$ ls /challenge
3311-renamed-run-15569  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/3311-renamed-run-15569
Yahaha, you found me! Here is your flag:
pwn.college{ItWXkvtDKA9pjEi13CS8UR_Ph1j.QX4IDO0wiN5gjNzEzW}```
