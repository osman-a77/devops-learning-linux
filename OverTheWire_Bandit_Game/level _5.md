# Level 4 → Level 5

## Challenge
The password for next level is stored in the only human-readable file in the inhere directory.

## Solution
```
cd inhere
ls
file ./*
cat ./-file07
```

## Explanation
There are 10 files in the files in the inhere directory of which only one is in human-readable format. Therefore, you must use the file
command which will classify each file and the one which is in human-readable format will display ASCII text.

## Password
6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG

## What I learned
Instead of using the file command on each individual file you can do file ./* which will perform the file command on all files
simultaneously.
