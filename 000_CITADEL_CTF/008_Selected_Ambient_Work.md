# SELECTED AMBIENT WORK
“The symphonic adventure does not end here. On the next floor, a single song keeps echoing through the floor, repeating in a 
haunting loop. Amid the sound, you find a note left by a past candidate. It hints that the song holds a secret message, hidden in 
plain sight, much like how Aphex Twin concealed his face within his music with the help of spectrograms.
To move forward, you must find the message hidden in this sound.
Note: Separate the words in the flag with _ and make it UPPERCASE. Example: citadel{S3L3CT3D_AMB13NT_W0RK}” 

## MY SOLVE
**Flag:** ` citadel{1_LOV3_1DM}`

### THOUGHT PROCESS/STEPS
In this challenge, we were provided with an audio file, when listened to the audio file we realized that it was morse code but the 
twist was that it had a considerable amount of background music so do make the morse code clearer we had to clear aout the 
background music, we used audacity for that purpose first we went on analyse-plot spectrum to figure out what was the peak 
frequency for a beep i.e 1000hz then I went to effects applied high pass filter then low pass filter and then did some 
amplification to get the beeps louder and lil isolated then rest of the audio then finally I exported the new audio and used an 
online morse code decoder site to decrypt the audio file which gave me what was said in the audio the text came out to be 
“RICHARD D JAMES AKA APHEX TWIN IS A BRITISH MUSICIAN, COMPOSER AND DJ ACTIVE IN ELECTRONIC MUSIC SINCE 1988 1 L0V3 1DM AND IS A 
PIONEERING FIGURE IN THE INTELLIGENT DANCE MUSIC IDM GENRE.”  The odd part from this was 1 L0V3 1DM which was basically but the 
content of the flag.

## REFERENCES 
https://www.audacityteam.org/
https://morsecode.world/international/decoder/audio-decoder-adaptive.html

## WHAT I LEARNT 
Learnt the process of decoding a morse code.
