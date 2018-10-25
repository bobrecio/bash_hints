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
>> history | grep cat
 >10 cat file9.txt
 >11 cat file0.txt
 >33 cat this.txt
 >453 cat this.txt
 >513 vi catalog
>> !453
>> cat this.txt
>```
