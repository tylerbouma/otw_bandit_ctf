**PW:** Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI

**Instructions:** A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

First we will go back to */etc/cron.d/* to look at the *cronjob_bandit23*

We see that it runs a script called */usr/bin/cronjob_bandit23.sh*:
```
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
```

The script is essentially copying out the bandit* user's password to a file under /tmp/

We can find the file that bandit23 may be using by manually running the **mytarget** variable assignment.

`echo I am user $myname | md5sum | cut -d ' ' -f 1`

This tells us that the bandit23 password is stored in a file called */tmp/8ca319486bfbbc3663ea0fbe81326349*

`more /tmp/8ca319486bfbbc3663ea0fbe81326349`

**Flag:** jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n
