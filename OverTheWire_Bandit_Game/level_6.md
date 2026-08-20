# Level 5 → Level 6

## Challenge
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

##### human-readable
##### 1033 bytes in size
##### not executable

## Solution
```
cd inhere
find . -type f -size 1033c ! -executable
cat ./maybehere07/.file2
```

## Explanation
The find command allows you to look for a file or directory with specific conditions. So by tailoring command line to specific conditions
required it printed location of that file. Finally cat command reads its contents and produces password.

## Password
pXa26xhMWaC2SvDotA4r9EgZkulOeSBW

## What I learned
The find command is extremely powerful and useful when searching for specific files or directories.
