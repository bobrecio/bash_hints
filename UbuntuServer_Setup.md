##Linux Server setup##
####1. Install####
####Start SSH###
If you set up ssh first, you can do the rest remotely.
$ sudo apt install tasksel
$ sudo tasksel -> Turn on openssh server
$ apt install byobu
$ sudo apt install zfsutils-linux
$ sudo zpool import zpool01
$ blkid /dev/sdc1 (get UUID for use as /home)
$ 
$ sudo tasksel -> turn on LAMP server
$ln -s /zpool01/HOME/www /www
$ mv /var/www/html /var/www/html.orig
$ln -s /var/www/html /www
$ sudo mysql_secure_installation
