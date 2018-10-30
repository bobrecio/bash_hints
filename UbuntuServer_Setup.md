Linux Server setup
==================

1. Install Ubuntu Server from USB<br>
>- Install the root to, at least, a 40Gb partition. 100Gb should be enough.<br>
>- Map ```/home``` to a large ext4 partition (if possible) (we can add it in fstab later)<br>
>- If you are dual booting with Windows, consider mapping a vfat partition to ```/dos```, then you can share content with Windows.<br>

2. Set up SSH first so you can do the rest remotely!<br>
```$ sudo apt install tasksel```<br>
```$ sudo tasksel``` -> Turn on openssh server<br>

2. Install byobu so you can run installs and walk away<br>
```$ apt install byobu```<br>

3. Install ZFS, import zpool01<br>
```$ sudo apt install zfsutils-linux```<br>
```$ sudo zpool import zpool01```<br>

4. Mount ```/home```, ```/dos```, ```/hd01```<br>
Get UUID of partition<br>
```$ blkid /dev/sdc1```<br>
```$ln -s /zpool01/HOME/www /www```<br>

5. Turn on LAMP server using tasksel<br>
```$ sudo tasksel``` -> turn on [*]LAMP server<br>

6. Create alternate location for www<br>
```$ mv /var/www/html /var/www/html.orig```<br>
```$ln -s /var/www/html /www```<br>

7. Secuter the mysql instance<br>
```$ sudo mysql_secure_installation```<br>

8. Add ```index.php``` and ```default.php``` to be executable by apache2.<br>

9. Add your account to www-data<br>
```sudo vi /etc/group```<br>

1. Plexmediaserver => https://www.plex.tv/media-server-downloads/


