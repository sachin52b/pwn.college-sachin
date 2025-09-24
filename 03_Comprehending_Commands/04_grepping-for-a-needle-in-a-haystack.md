# Grepping-for-a-needle-in-a-haystack

This challenge expected us to find the flag from a text file in a particular path in which the flag was given in a particular line. 

## My solve
**Flag:** `pwn.college{wMz34iAr1eQaTIc1rnAjCtq4dZs.QX3EDO0wiN5gjNzEzW}`

### Thought process

The thing was very basic that we had to use grep command to print the particular line from the file which had the flag in it so i just wrote grep cmd with arguments pwn.college(as the line with flag was starting from "pwn.college" only) and the path to file.



```bash
:~$ grep pwn.college /challenge/data.txt
pwn.college{wMz34iAr1eQaTIc1rnAjCtq4dZs.QX3EDO0wiN5gjNzEzW}```
