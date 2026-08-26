# Level 13 → Level 14

## Challenge
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t 
get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you in
to previous bandit levels, and find out how to use the key for this level.

## Solution
```
cat sshkey.private
```
```
ssh -i private.key bandit14@bandit.labs.overthewire.org -p 2220
```

## Explanation
For this level you aren't given a password but an ssh key so you must use cat command to read it and then copy the contents. Then you paste
the ssh key into a file in your home directory(here I've named the file private.key). Finally you can use the ssh key along with the 
command ssh -i to log into the next level.

## What I learned
Here you understand that ssh can authenticate you using a private key instead of a password.
