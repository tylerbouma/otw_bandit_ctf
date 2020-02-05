**PW:** UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ

This level has a daemon listening on port 30002. This takes the level 24 password and a secret pin 0000 - 9999 *ex. UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ 1111**
The process of brute forcing all pins is easy as long as you can write out a list of them.
Luckily */var/spool/bandit24** is available with write privileges. The unfortunate part is that the directory wipes out files constantly via a cron job.
The trick was creating a directory and then creating a txt file with all variations of the pin (via bash script).

`nc localhost 30002 < pinlist.txt` does the trick from here.

**Flag:** uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG
