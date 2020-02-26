This is a **crazy** and creative level design.

We are first given a bandit26.sshkey file under /home/bandit25.

``` ssh -i bandit26.sshkey bandit26@localhost.org ```

This gives us SSH access to bandit26, but when doing so we find that the session closes immediately.
Since the instructions give us a hint that a "different" shell is being used, we can go ahead and do a `cat /etc/passwd | grep bandit26`.
I now see it is using something called */usr/bin/showtext*.

After a closer inspection I see that this calls on a *~/text.txt* file and then immediately exits.

The **crazy** part of this comes with how we can stall this exit mechanic. By minimizing the terminal window enough to the point of the text.txt text not being able to display completely, we are given a **more** option.
We can then type "v" to give us a vim session and then by typing `:e /etc/bandit_pass/bandit26` we can access the password file - giving us the password to bandit26.

Note that this flag doesn't really do anything for us since we already have an SSH key.

**Flag: (not really)** 5czgV9L3Xx8JPOyRbXh6lQbmIOWvPT6Z

We are still connected to bandit26 via a VIM session.

While still in our VIM session we need to first change the shell we are using so we can actually run commands. To do this we use shell=/bin/bash. This will grant us access to the functionality of bash. We can now run commands for vim using :! <command>

Let's try :! ls

Returns: text.txt and bandit27-do. bandit27-do sounds interesting.

:! bandit27-do

Run a command as another user. Example: ./bandit27-do id

So this looks like it allows us to run commands as the bandit27 user - let's try grabbing the password from /etc/bandit-pass/badit27

:! ./bandit27-do cat /etc/bandit_pass/bandit27

**Flag:** 3ba3118a22e93127a4ed485be72ef5ea
