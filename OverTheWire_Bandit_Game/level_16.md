# Level 15 → Level 16

## Challenge
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using 
SSL/TLS encryption.

## Solution
```
openssl s_client -connect localhost:30001
```

## Explanation
The first part of the command, openssl s_client, establishes a tls connection and the second part, -connect localhost:30001, specifies
which host and port number to connect to. After that the command line will expect you to input something which here would be the password 
for the current level and in turn it will print the password for the next level.

## Password
kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V

## What I learned
You can use openssl s_client command to establish a tls connection and it also has a variety of useful extensions.
