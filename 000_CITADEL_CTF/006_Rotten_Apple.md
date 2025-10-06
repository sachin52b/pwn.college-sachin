# ROTTEN APPLE
“Among the debris of this floor, you find a relic of sound: An album which turns out to be D>E>A>T>H>M>E>T>A>L by Panchiko, a long 
lost album. But the music is warped, as though it has undergone disc rot.

The path forward is hidden in the distortion. Similar to how the album was warped, the password to the next floor has been warped 
first by a factor of 47, then by a factor of 13. Untangle these changes to reveal the code and continue your ascent.

4:R256=Y3oRRoP0#~%Ro?A” 

## MY SOLVE
**Flag:** ` citadel{b3tt3r_ROTt3n}`

### THOUGHT PROCESS/STEPS
In this challenge, the description mentioned that the flag had been “warped” first by a factor of 47 and then by 13 — in other 
words, it had been rotated by 47 and then by 13. Undoing this was just a matter of reversing the rotations.
What we did was take the provided text:
4:R256=Y3oRRoP0#~%Ro?A
First, we googled ROT13, found a site to apply it, pasted the text, and got the output:
4:E256=L3bEEbC0#~%Eb?N
Next, we took this result, searched for ROT47, pasted it into a ROT47 tool, and after rotating, we finally got the flag.
The trickiest part was understanding what the description meant by “warping” → rotation. That wasn’t obvious at first, but hints 
like the challenge name and the phrase “disc rot” pointed us toward ROT ciphers, guiding us to the correct method.

## REFERENCES 
https://rot13.com/
https://www.dcode.fr/rot-47-cipher

## WHAT I LEARNT 
Learnt about ROT ciphers.

