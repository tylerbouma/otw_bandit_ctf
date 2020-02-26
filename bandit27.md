**PW:** 3ba3118a22e93127a4ed485be72ef5ea

This next level is realatively simple and involves cloning a git repository.

There is a git repository at ssh://bandit27-git@localhost/home/bandit27-git/repo. The password for the user bandit27-git is the same as for the user bandit27.

Clone the repository and find the password for the next level.

We will clone the repository to a directory in /tmp

`git clone ssh://bandit27-git@localhost/home/bandit27-git/repo /tmp/bandit27_clone`

cd to that directory and `cat` the **README** to find the flag 

**Flag:** 0ef186ac70e04ea33b4c1853d2526fa2
