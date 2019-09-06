## alias
```alias ll='ls -l'```
## apt
```sudo apt update && sudo apt upgrade -y```
## awk
## cat
```cat ~/.bashrc```
## cd
```cd /home```
## chmod
```chmod +755 [bash script file]```
## chown
```chown +R user:user [folder or file]```
## chsh
````chsh -s [/bin/bash,/bain/zsh,etc]```
## clear
## cp
```cp -rfv source target/```
## curl
## df
## diff
## du
## echo
## egrep
## exit
## find
## finger
## free
## gparted
## groups
## gzip
## head
## history
## ifconfig
## less
## locate
## ls
## lsblk
## lsb_release -a
- shows distro and OS info
## man
## mkdir
## mv
## netstat
## passwd
## ping
## ps
## pwd
## python3 -m http.server
- servers the current folder in browser
```python3 -m http.server```

## reboot
## rm
## rmdir
## rsync
## sed
## shutdown
## ssh
## su
## sudo
## tail
Use ‘tail’ to monitor logs real-time for bug reporting or system analysis. This will provide you updates that occur and could be invaluable for bug reports or monitoring of user activity or changes on your system.

As an example:

For openSUSE, Rhel you can use:
sudo tail -f -n 6 /var/log/messages

For Debian based distros
sudo tail -f -n 6 /var/log/syslog

The ‘f’ switch tells it to follow
The ‘n’ switch tells it to display last N’th number of lines
## tar
## top
## touch
## tree
- HTML(-H):  
```tree -H '.' -L 1 --noreport --charset utf- -o tree.html```
- JSON(-J):  
```tree -a -J -o tree.json```
## uname
## vi
## w
## wc
## wget
## who
## whoami
## zip