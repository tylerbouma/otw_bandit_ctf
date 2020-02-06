This is a **crazy** and creative level design.

We are first given a bandit26.sshkey file under /home/bandit25.

``` ssh -i bandit26.sshkey bandit26@localhost.org ```

This gives us SSH access to bandit26, but when doing so we find that the session closes immediately.
Since the instructions give us a hint that a "different" shell is being used, we can go ahead and do a `cat /etc/passwd | grep bandit26`.
I now see it is using something called */usr/bin/showtext*.

After a closer inspection I see that this calls on a *~/text.txt* file and then immediately exits.

The **crazy** part of this comes with how we can stall this exit mechanic. By minimizing the terminal window enough to the point of the text.txt text not being able to display completely, we are given a **more** option.
We can then type "v" to give us a vim session and then by typing `:e /etc/bandit_pass/bandit26` we can access the password file - giving us the flag.

**Flag:** 5czgV9L3Xx8JPOyRbXh6lQbmIOWvPT6Z
