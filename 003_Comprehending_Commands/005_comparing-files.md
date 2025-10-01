# Comparing-files

This challneg expected us to find the real flag by using diff between 2 files. 

## My solve
**Flag:** `pwn.college{IBbuVp773V-LLSEDSSydeQ2HNfX.01MwMDOxwiN5gjNzEzW}`

### Thought process

two file with their paths were given one had fake flags and one had fake flags+one real flag so this was basically the main difference that came out when we used diff command.



```bash
~$ diff /challenge/decoys_and_real.txt /challenge/decoys_only.txt
86d85
< pwn.college{IBbuVp773V-LLSEDSSydeQ2HNfX.01MwMDOxwiN5gjNzEzW}```
