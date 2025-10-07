# SELECTED AMBIENT WORK
“The symphonic adventure does not end here. On the next floor, a single song keeps echoing through the floor, repeating in a 
haunting loop. Amid the sound, you find a note left by a past candidate. It hints that the song holds a secret message, hidden in 
plain sight, much like how Aphex Twin concealed his face within his music with the help of spectrograms.
To move forward, you must find the message hidden in this sound.
Note: Separate the words in the flag with _ and make it UPPERCASE. Example: citadel{S3L3CT3D_AMB13NT_W0RK}” 

## MY SOLVE
**Flag:** ` citadel{1_LOV3_1DM}`

### THOUGHT PROCESS/STEPS
In this challenge, we were provided with an audio file. When we listened to it carefully, we realized that the beeping pattern in the audio resembled Morse code, but there was a significant challenge — the background music was extremely loud and made it hard to distinguish the actual Morse beeps.

To isolate the Morse signals, we used Audacity, an audio editing tool. First, we opened the file in Audacity and went to Analyze → Plot Spectrum to inspect the frequency components of the audio. This allowed us to determine the peak frequency of the Morse beeps, which turned out to be around 1000 Hz.

Once we identified the frequency, we began filtering out the unwanted noise. We applied a High-Pass Filter(val=990 HZ) to remove the low-frequency background elements, followed by a Low-Pass Filter(1010 HZ) to eliminate the higher-frequency background sounds, leaving only the midrange tone of the beeps. After filtering, we performed amplification to make the Morse tones clearer and more prominent compared to the background audio.

With the Morse beeps now relatively isolated, we exported the cleaned audio and uploaded it to an online Morse code decoder website. The site successfully decoded the beeping pattern into readable text, which turned out to be:

“RICHARD D JAMES AKA APHEX TWIN IS A BRITISH MUSICIAN, COMPOSER AND DJ ACTIVE IN ELECTRONIC MUSIC SINCE 1988 1 L0V3 1DM AND IS A PIONEERING FIGURE IN THE INTELLIGENT DANCE MUSIC IDM GENRE.”

Most of the text was an informative description about Aphex Twin, a famous electronic musician, but one segment clearly stood out — “1 L0V3 1DM” — which didn’t fit naturally with the rest of the text. This unusual phrase was the actual flag for the challenge.

Thus, by methodically cleaning the audio, isolating the Morse beeps, and decoding the message, we successfully extracted the hidden flag.

## REFERENCES 
https://www.audacityteam.org/
https://morsecode.world/international/decoder/audio-decoder-adaptive.html

## WHAT I LEARNT 
Learnt the process of decoding a morse code.
