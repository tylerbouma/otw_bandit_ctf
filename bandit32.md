**PW:** 56a9bf19c63d650ce78e6ec0354ee45e

This is another level where we need to escape a very annoying shell. This shell converts everything typed to UPPERCASE.

Luckily we can exectute the shell again and escape by using `$0`. Since *uppershell* has a setguid flag for the bandit33 user we can easily gain access to that user.

Once we have the bandit33 user we can easily look in */etc/bandit_pass/bandit33* and find the flag:

**Flag:** c9c3199ddf4121b10cf581a98d51caee
