# Level 18 → Level 19

## Challenge
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out
when you log in with SSH.

## Solution
```
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```

## Password
IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

## Explanation
Here we're immediately logged out when trying to connect and we also know that the password is stored in a file called readme. If you write
a command at the end when trying to connect with ssh it will execute it before you're logged out. Here we need the cat command to show
contents of readme file.

## What I learned
It's important to go over the man pages of common commands as an option can solve problem.
