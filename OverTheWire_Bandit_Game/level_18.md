# Level 17 → Level 18

## Challenge 
There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the 
only line that has been changed between passwords.old and passwords.new

## Solution 
```
diff passwords.old passwords.new 
```

## Explanation
Here using the diff command will output the changed line which is the password. It first shows what the line was in the passwords.old file
and then what it is now in the passwords.new file. The password is the second line.

## Password
kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

## What I learned
The diff command is essential when comparing files.
