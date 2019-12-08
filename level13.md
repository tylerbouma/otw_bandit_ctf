PW: **8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL**

We are given access to a private key file names *sshkey.private*. This will be used to log into bandit14.
We need to grab that file from the remote server and bring it back to our host.

`scp` is our friend here: `scp -P 2220 bandit13@bandit.labs.overthewire.org:~/sshkey.private /Users/tylerbouma/`.
This reaches out to the remort server (on port 2220) and copies the file to our local machine.

Also be sure to `chmod 600 sshkey.private` otherwise you will not be able to use it for level 14.

Once we are on bandit14, let's grab the flag from */etc/bandit_pass/bandit14* for good measure.

Flag: **4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e**
