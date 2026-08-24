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
