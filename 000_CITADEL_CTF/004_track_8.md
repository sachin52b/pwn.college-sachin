# TRACK 8
“Bypassing the second chamber leads to an empty floor except for a single artifact in the center: an old MP3 player, scratched 
and worn. On its surface, a cipher is etched, a message left behind for anyone who can decode it:
twj eys zpr ukm 'viamnwqw' bx lzgo: esmqqui{yyr_oshwwcm_bwupa}
When you power it on, the sound fills the chamber. The tracks play like whispers from a lost world, and you recognize it as a song 
from Panchiko’s latest studio album, particularly track no. 8. Its title feels familiar, hinting at a famous cipher. Decrypt it 
by using the album name as your key and continue your ascent.” 

## MY SOLVE
**Flag:** ` citadel{add_vinegar_twice}`

### THOUGHT PROCESS/STEPS
After carefully reading the full description, the first hint that caught our attention was “Panchiko’s latest studio album.” We 
googled that exact phrase and found that the album was Ginkgo. Next, we checked the 8th track of this album and discovered its title — 
“Vinegar.”
The challenge description also mentioned that this title hinted toward a particular cipher. Seeing the word vinegar, we immediately 
searched “vinegar cipher” on Google, and the first result was actually a Vigenère cipher encoder/decoder website.

We used that site and entered the given encrypted text:

twj eys zpr ukm 'viamnwqw' bx lzgo: esmqqui{yyr_oshwwcm_bwupa}


using the key “Ginkgo” (as the challenge mentioned that the key was the album name).

This gave us a new encrypted output:

rigckmv{osd_ikumqog_tjkjm}


We noticed another clue in the description telling us to use this new text again with the key “PANCHIKO.” So, we decrypted the 
new text with that key — and that’s when we finally got our flag.

## REFERENCES 
https://cryptii.com/pipes/vigenere-cipher

## WHAT I LEARNT 
Learnt what is a cipher .

