PW: **DXjZPULLxYr17uwoI01bNLQbtFemEgo7**

This challenge hides the flag "somewhere on the server". The only clues we are given are:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

Again, we will use the find command: `find /* -type f -size 33c -user bandit7 -group bandit6 2>/dev/null | xargs ls -la`.
This will return a file meeting all of the criteria, while hiding the "permission denied" errors.
We find it hidden in */var/lib/dpkg/info/bandit7.password*

Flag: **HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs**
