We are still connected to bandit26 via a VIM session.

While still in our VIM session we need to first change the shell we are using so we can actually run commands. 
To do this we use `shell=/bin/bash`.
This will grant us access to the functionality of bash.
We can now run commands for vim using `:! <command>`

Let's try `:! ls`

Returns: **text.txt** and **bandit27-do**. bandit27-do sounds interesting.

`:! bandit27-do`

*Run a command as another user.*
*Example: ./bandit27-do id*

So this looks like it allows us to run commands as the bandit27 user - let's try grabbing the password from */etc/bandit-pass/badit27*

`:! ./bandit27-do cat /etc/bandit_pass/bandit27`

Flag: 3ba3118a22e93127a4ed485be72ef5ea
