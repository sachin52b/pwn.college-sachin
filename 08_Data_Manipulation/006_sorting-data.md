# Sorting-data
The challenge’s purpose was to make us explore the use of sort command which basically arranges the dat of files in 
ascending order(by default) with the use of several other kind of arguments we can change how sort cmd works.

## My solve
**Flag:** ` pwn.college{8TSil4DDHZ8rVddsByn-TtMpiRX.0FM0MDOxwiN5gjNzEzW} `

### Thought process/Steps
The steps were simple and straightforward. First, I used sort -r to list the contents of the file in descending order. Since the 
question mentioned that in ascending order the flag would be at the last position, in descending order it appeared at the first position.
I then piped this output to head -n 1 to extract the first line, which was the flag.
 
```bash
~$ sort -r /challenge/flags.txt | head -n 1
pwn.college{8TSil4DDHZ8rVddsByn-TtMpiRX.0FM0MDOxwiN5gjNzEzW} 
```
