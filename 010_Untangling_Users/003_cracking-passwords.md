# Cracking-passwords
The challenge’s purpose was to mainly  make us learn the use of a passwd cracking tool 
JOHN-THE RIPPER.


**Flag:** ` pwn.college{EFpBE2pCni27XlVswgnqXjmNGv3.QX3UDN1wiN5gjNzEzW} `

### Thought Process/Steps
This challenge felt different from the earlier ones because we weren’t handed the password — we had to crack it ourselves. 
The prompt mentioned john (John the Ripper) as the tool to use, so I figured I needed to feed it the password-hash file. 
I ran john path_to_shadow_file to let John generate candidate passwords, hash them, and compare those hashes to the ones in the file. 
When a candidate’s hash matched an entry in the shadow file, John revealed the password. With the cracked password for zardus in 
hand, I used su zardus, entered the password, and then invoked /challenge/run to get the flag.

```bash
~$ john /challenge/shadow-leak
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04962g/s 288.9p/s 288.9c/s 288.9C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{EFpBE2pCni27XlVswgnqXjmNGv3.QX3UDN1wiN5gjNzEzW}```

