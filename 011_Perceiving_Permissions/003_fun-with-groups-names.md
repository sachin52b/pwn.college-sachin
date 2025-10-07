# FUN-WITH-GROUPS-NAMES
The challenge expected to us to learn and implement how to change the group ownership of a file but first it wanted us to figure 
out what group are we in.

## MY SOLVE
**Flag:** ` pwn.college{M26JL8UNSPfacvLYDxYAKp9u1kT.QXycjM1wiN5gjNzEzW}`

### THOUGHT PROCESS/STEPS
There was a twist in this challenge compared with the previous one: the “hacker” wasn’t listed as part of a known hacker group — their 
group name had been renamed, so I couldn’t tell which group they belonged to at a glance. That made me think: the question clearly 
hinted to check the user’s identity, so I ran id to see their UID and group memberships. The output showed the group grp26298, so 
I knew which group I needed to target. Next I changed the group ownership of /flag from root to grp26298 using chgrp grp26298 /flag. 
With the file now accessible to that group, I simply ran cat /flag and retrieved the flag.

```bash
~$ id
uid=1000(hacker) gid=1000(grp26298) groups=1000(grp26298)
hacker@permissions~fun-with-groups-names:~$ chgrp grp26298 /flag
hacker@permissions~fun-with-groups-names:~$ ls -l /flag
-r--r----- 1 root grp26298 60 Oct  7 08:21 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{M26JL8UNSPfacvLYDxYAKp9u1kT.QXycjM1wiN5gjNzEzW}
```
