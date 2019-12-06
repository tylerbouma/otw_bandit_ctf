PW: **HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs**
 
The only clue we are given:
- The password for the next level is stored in the file data.txt next to the word millionth

When looking at the home directory we find the *data.txt* file which contains a large list of words and then strings.
To find the key belonging with "millionth" I simply: `cat data.txt | grep millionth`.
That will find the line containing millionth and print it to the screen.

Flag **cvX2JJa4CFALtqS87jk27qwqGhBM9plV**
