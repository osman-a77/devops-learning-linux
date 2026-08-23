# Level 11 → Level 12

## Challenge
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated
by 13 positions

## Solution
```
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

## Explanation
The tr command can translate characters from one set to another so here the second set represents each letter if it were moved 13 positions 
forward in the alphabet which would essentially return line of text back to its original format.

## Password
GROozWPO8QyN0mGrjUkID0WCYkZiQxrN

## What I Learned
Knowing how to correctly format each set is crucial when using the tr command.
