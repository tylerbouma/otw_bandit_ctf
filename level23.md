**PW:** jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n

**Instructions:** A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

We first check out what's going on in */usr/bin/cronjob_bandit24.sh*

```
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname
echo "Executing and deleting all scripts in /var/spool/$myname:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        timeout -s 9 60 ./$i
        rm -f ./$i
    fi
done
```

This appears to be executing all files under */var/spool/bandit24*... Interesting. We will use a cronjob_bandit23.sh script copy and paste it in
the /var/spool/bandit24 directory (774 permissions). This causes the bandit24 password to be written out under the /tmp/ directory.

Running `echo I am user $myname | md5sum | cut -d ' ' -f 1` tells us that the password is written out under */tmp/ee4ee1703b083edac9f8183e4ae70293*

**Flag:** UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
