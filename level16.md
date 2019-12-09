PW: **cluFn7wTiGryunymYOu4RcffSxQluehd**

Clue: The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

First we do a cursory check of the ports that are open using `nmap`

`nmap localhost -p31000-32000`

returns:

Starting Nmap 7.40 ( https://nmap.org ) at 2019-12-09 19:30 CET

Nmap scan report for localhost (127.0.0.1)

Host is up (0.00028s latency).

Not shown: 999 closed ports

PORT      STATE    SERVICE

31518/tcp filtered unknown

31790/tcp open     unknown

Nmap done: 1 IP address (1 host up) scanned in 1.26 seconds

We use `openssl s_client -connect localhost:31790` and paste the password. We are then given a private key that we will use for level 17.

Retrieve the key using scp: `scp -P 2220 bandit16@bandit.labs.overthewire.org:/tmp/gr0k2/lvl17.key /Users/tylerbouma`
