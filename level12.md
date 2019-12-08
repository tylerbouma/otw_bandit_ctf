PW: **5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu**

Clue: The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!).

This is an interesting one... The original file is a hex dump of a binary file.

First we use `xxd -r data.txt data.bin`. This will revert the hex dump back to a binary file.

We then use the `file` command to find out the .bin file is compressed.
We then begin the process of uncompressing the file multiple times from either a: gzip, bzip2, or tar format.
Use the `file` command after each decompression to find out what the next level of compression is.

Flag: **8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL**
