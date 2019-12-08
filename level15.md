PW: **BfMYroe26WYalil77FoDi9qh59eK5xNr**

Clue: The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

We are also given https://www.feistyduck.com/library/openssl-cookbook/online/ch-testing-with-openssl.html# to reference.

Using `openssl s_client -connect localhost:30001` we are able to open a secure connection and paste our password.

Flag: **cluFn7wTiGryunymYOu4RcffSxQluehd**
