# bash_hints
These are some clips that I've found around the internet to remind myself how to do different things in BASH
***
### Looping through files ###
>```
>for file in ./*.mp3; do
>    [ -e "$file" ] || continue
>    some command "$file"
>done
>```
***
### Use "" when performing commands on unknown filenames ###
#### _ALSO_... use "--" to let cp know that no more options follow, in case of files with leading "-" ####
>```
>cp -- "$file" "$target"
>```
***
### Use *printf* instead of *echo* ###
#### for example, echo may interpret "-n" as an option ####
>```
>printf "%s\n" "$foo"
>```
***
### Execute a command from *history* ###
>```
>$ history | grep cat
 >10 cat file9.txt
 >11 cat file0.txt
 >33 cat this.txt
 >453 cat this.txt
 >513 vi catalog
>$ !453
>> cat this.txt
>```
***
### Get UUID of disk (for fstab) ###
>```
>$ blkid /dev/sdc1
>/dev/sdc1: UUID="365c77f7-3bfc-4557-a63f-d8132114293a" TYPE="ext4" PARTLABEL="HOME" PARTUUID="626068f0-d7db-411f-a7a5-65b5b554d299"
>```
...or...
>```
>$ ls -l /dev/disk/by-uuid
>total 0
>lrwxrwxrwx 1 root root 10 Oct 25 21:37 13594347858422367081 -> ../../sdb1
>lrwxrwxrwx 1 root root 10 Oct 25 21:37 1E15-1D04 -> ../../sdb3
>lrwxrwxrwx 1 root root 10 Oct 25 21:37 20e6c1e0-717c-4f68-9ece-ad7041266ea3 -> ../../sdc2
>lrwxrwxrwx 1 root root 10 Oct 25 21:37 30f9465e-a5d8-4474-8096-d4201258c12b -> ../../sda2
>lrwxrwxrwx 1 root root 10 Oct 25 21:37 365c77f7-3bfc-4557-a63f-d8132114293a -> ../../sdc1
>lrwxrwxrwx 1 root root 10 Oct 25 21:37 a46ed437-3a9d-409c-9a04-68c4c5c26c8b -> ../../sdc3
>```
### Create directory containging date (for backup files) ###
>```mkdir $(date '+%Y.%m.%d.%H%M%S')```
***
### Create photo thumbnails and resize ###
>```
>#! /bin/bash
>for i in *.jpg; do
>        convert "$i" -resize 200x150 "th.$i";
>        convert "$i" -resize 1024x768 "web.$i";
>done;
>```
