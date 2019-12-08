PW: **UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR**

We are given a *mostly* binary file with bits of human readable strings. The goal is to find a flag that is preceded by "several ‘=’ characters".
To do this we use the `strings` command:

`strings data.txt | grep ==*`

This outputs any human readable (ASCII) string and then we grep for items preceded by 1+ '=' signs.

*========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk* <- This look right to me.

Flag: **truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk**
