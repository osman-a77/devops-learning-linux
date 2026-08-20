# Level 3 → Level 4

## Challenge
The password for the next level is stored in a hidden file in the inhere directory.

## Solution
```
cd inhere
ls -a
cat ...Hiding-From-You
```

## Explanation
Since password is in the inhere directory you must first change to that directory. Then you must use ls -a command which will show all
contents of directory including hidden files. Finally using cat command you can find password.

## Password
xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq

## What I learned
It's important to know different variations of commands such as ls -a since they can be used to solve specific issues.
