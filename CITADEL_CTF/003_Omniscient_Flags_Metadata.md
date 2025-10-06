# OMNISCIENT FLAG'S METADATA

“As you step into the second chamber, a figure manifests. Before you stands a forgotten deity, a dead god spoken of only in 
whispers. Known by countless names: “Apostle of Epilogue and Eternity”, “Lone Messiah” and many more lost to time.They leave nothing 
but a single image, a relic carrying his final secret. Hidden within its layers lies the key to ascend to the next chamber.” 

## MY SOLVE
**Flag:** ` citadel {th1s_ch4ll3ng3_1s_f0r_th4t_On3_ex1ft00l_4ndb1nw4lk_enthus14st}`

### Thought Process/Steps
In this challenge, we first downloaded the given JPG file and then searched online for an Exif tool, since the challenge hinted that 
the image contained hidden metadata. Using the tool, we checked the metadata and noticed a clue in the author name field — it 
hinted that there was another image hidden inside this one. Following that lead, we searched for an image layer extractor and found 
a website called Aperisolve. We uploaded the image there, and it provided us with a downloadable ZIP file containing the extracted 
layers. Inside that ZIP, we found a PNG image — and that image had the flag written on it.


## References 
https://exif.tools/
https://aperisolve.fr/

## What I learnt 
Learnt the use of exif and binwalk tools.
