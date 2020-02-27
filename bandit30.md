**PW:** 5b90576bedb2cc04c86a9e924ce42faf

In this level we are given another git repository, but the **README.md** only reads: 
>just an epmty file... muahaha

I check for branches, but there aren't any other than the master - dead end.

After a bit of googling and `ls` I find that there is a tag called "secret" - interesting. I'm not able to checkout the tag as it doesn't belong to anything, but I can do a `git show secret`

This returns something that looks like a flag, so let's give it a try...

Success!

**Flag:** 47e603bb428404d265f59c42920d81e5
