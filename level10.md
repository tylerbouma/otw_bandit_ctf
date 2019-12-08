PW: **truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk**

Clue: The password for the next level is stored in the file data.txt, which contains base64 encoded data

This is relatively simple after taking a peak at the `base64` man page. `base64 -d data.txt` returns *The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR*

Flag: **IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR**
