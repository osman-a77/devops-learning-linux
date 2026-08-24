# Level 12 → Level 13

## Challenge
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this 
level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, 
use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Solution
```
mkdir /tmp/osman
cp data.txt /tmp/osman
cd /tmp/osman
xxd -r data.txt > data
file data
mv data data.gz
gzip -d data.gz
ls
file data
mv data data.bz2
bzip2 -d data.bz2
ls
file data
mv data data.gz
gzip -d data.gz
ls
file data
mv data data.tar
tar xf data.tar
ls
file data5.bin
mv data5.bin data5.bin.tar
tar xf data5.bin.tar
ls
file data6.bin
mv data6.bin data6.bin.bz2
bzip2 -d data6.bin.bz2
ls
file data6
mv data6 data6.tar
tar xf data6.tar
ls
file data8.bin
mv data8.bin data8.bin.gz
gzip -d data8.bin.gz
ls
file data8
cat data8
```

## Explanation
For this challenge the password has been stored in a hexdump of a file that has been repeatedly compressed and archive, therefore, the
solution here is to decode, decompress and unarchive until the file is in a human-readable format. Firstly you must create a new 
directory and copy data.txt there in order to protect the original file. Then using the xxd -r command you can reverse the hexdump. This
followed by a repeated process of checking file type, rename with correct file extension and decompressing. If it's a gzip compressed data
file then use gzip -d command to decompress and if it's a bzip2 compressed data file then use bzip2 -d command to decompress. If the file
is a tar type then use tar xf to extract file. Eventually there will be a file that is an ASCII text type in which you then use the cat
command and retrieve solution.

## Password
qQYQiHOBPR8zR61qxYqX45quvihF2uzk

## What I learned
Renaming file with extension can help with visual clarity and avoid mistakes when going through repetitive process. The man command is 
very powerful and directly helps here to know what command to use to decompress. Also knowing file types can help with executing next
command.
