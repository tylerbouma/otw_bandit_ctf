**PW:** 0ef186ac70e04ea33b4c1853d2526fa2

This is another puzzle where we are asked to clone a git repository, but in this case we aren't immediately given the password in the *README*

After cloning the repository we are presented with a *README.md*, which contains

>Bandit Notes
>
>Some notes for level29 of bandit.
>
>credentials
>
>- username: bandit29
>- password: xxxxxxxxxx

This would be a pretty useless file if it never contained the password, so let's look at the git commit logs: `git log -p -2`

After reading through this log it becomes apparent that the password was changed from bbc96594b4e001778eee9975372716b2 to xxxxxxxxxx.

**Flag:** bbc96594b4e001778eee9975372716b2
