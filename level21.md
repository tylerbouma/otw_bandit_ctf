**PW**: gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr

Instructions: A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

First we look under the /etc/cron.d/ directory to see what jobs exist. We find one called "cronjob_bandit22" - that sounds right. After doing a *more cronjob_bandit22* we find that it initiates a script called /usr/bin/cronjob_bandit22.sh

We can investigate that script to find this:

```
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```

We don't have permissions to run that script (only bandit22 does), but we can tell it is trying to write the bandit22 password to the file... Let's give that a try.

`more /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv`

Oh... 

**Flag**: Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
