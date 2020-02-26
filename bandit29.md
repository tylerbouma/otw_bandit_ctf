**PW:** bbc96594b4e001778eee9975372716b2

This is another level where we clone a git repository.

When we clone this directory and read the **README.md** we find the password has been redacted. 
When we look into the diffeent branches of this repository we find that there are a few:

`git branch -a`
>remotes/origin/HEAD -> origin/master

>remotes/origin/dev

>remotes/origin/master

>remotes/origin/sploits-dev

After checking out we find that the dev branch has the password contained in the **README.md**

**Flag:** 5b90576bedb2cc04c86a9e924ce42faf
