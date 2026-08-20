# Level 8 → Level 9

## Challenge
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## Solution
```
sort data.txt | uniq -u
```

## Explanation
The first part of the command sort data.txt will put identical lines next to each other and that output will inputted into second command
uniq -u which will omit identical lines. 

## Password
EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl

## What I learned
Commands don't have to be separated and can be combined using a pipe.
