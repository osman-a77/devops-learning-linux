# Level 9 → Level 10

## Challenge
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

## Solution
```
strings data.txt | grep '='
```

## Explanation
The first command extracts printable text strings from file and then outputs that into second command which highlights strings containing
=.

## Password
B0s2khmbT9u0geKuOoVGW3JZKhndE3BG

## What I learned
You can use strings command to extract printable strings from a file.
