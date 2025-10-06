# TEST OF SWEETNESS
“This floor feels like a digital world. The space is an illusion, all pink and sweet, stretching around you in impossible patterns. 
Here, you are no longer a climber but just another user.
Ahead, a door glows faintly. It is the only path forward and requires a level of authority you do not yet have. Fragments of session 
memory flicker, hinting at what it might take to gain higher access..” 

## MY SOLVE
**Flag:** ` citadel{fru1tc4k3_4nd_c00k13s}`

### THOUGHT PROCESS/STEPS
In this challenge, a link to a website was provided, and our main goal was to become the admin instead of a regular user. The first 
thing that came to our mind was to right-click and inspect the page — hoping to find something hidden in the source code or 
developer tools.All four of us started digging through the developer tools, exploring every tab — Elements, Console, Network, 
Application. Everything we could think of. It took quite a while, and honestly, it was a bit frustrating because nothing obvious 
showed up at first.But after carefully going through the details, we finally discovered what the challenge was hinting at — 
the cookie data as it said “session memory flicker” when we googled about it we came to know that session memory means temporary data 
and website’s temporary data is stored in cookies. We realized that by editing the cookie under application tab  and changing its 
value from user to admin, we could elevate our access level. Once we made that change and refreshed the page, we successfully 
became the admin and got the flag.

## REFERENCES 
https://testofsweetness.citadel.cryptonitemit.in/

## WHAT I LEARNT 
Learnt a simple way to take admin access of a website that if possible we could use a cookie edit if the website uses cookies .
