# Level 6 → Level 7

## Challenge
The password for the next level is stored somewhere on the server and has all of the following properties:

##### owned by user bandit7
##### owned by group bandit6
##### 33 bytes in size

## Solution
```
find / -type f -group bandit6 -user bandit7 -size 33c
cat /var/lib/dpkg/info/bandit7.password
```

## Explanation
Here you can use find command with specific conditions to find the file you're looking for. Since questions says it's somewhere in the 
server you should follow find command with forward slash which will start search at the root directory.

## Password
Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3

## What I learned
If you're looking for a file that is somewhere in the server you should use find / which will begin search at the root directory.
