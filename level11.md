PW: **IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR**

Clue: The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

After a bit of searching I found the `tr` command.

We can use something like `cat data.txt | tr '[a-z]' '[n-za-m]' | tr '[A-Z]' '[N-ZA-M]'` to rotate both the upper case and lower case letters. 
The *n-za-m* and *N-ZA-M* portion tells tr to rotate the letters by 13.

Output is: *The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu*

Flag: **5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu**
