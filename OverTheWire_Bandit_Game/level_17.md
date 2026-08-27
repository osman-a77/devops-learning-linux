# Level 16 → Level 17

## Challenge
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range
31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which 
don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Solution
```
nmap -p 31000-32000 localhost
nmap -p 31046,31518,31691,31790,31960 -A localhost
openssl s_client -connect localhost 31790
```

## Explanation
Here the first line of command scans the localhost between ports 31000 and 32000 for ports that speak ssl/tls and it produces 5 ports. 
The second line of command then scans those 5 ports for all information it has to determine which is listening. Once the correct port
has been determined you then use the last line of command to connect to it of which you then paste the password for this level. Here
we aren't given a password for the next level but an ssh key.

## What I learned
The nmap command is a very powerful command and can be used to scan ports and produce information on them.
