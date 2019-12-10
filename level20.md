PW: **GbKksEFF4yrVs6il55v6gwY5aVje5f0j**

Clue: There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think

First we need to setup a "listener" which will echo out the current password.

`echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -l localhost -p 61337 &`

We then run `./suconnect 61337` which then compares the current password with the string being echoed.

We are then givenRead: 
>GbKksEFF4yrVs6il55v6gwY5aVje5f0j

>Password matches, sending next password

>gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr

Flag: **gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr**
