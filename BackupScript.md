```
#!/bin/sh
dir=/home/backup/$(date '+%Y.%m.%d.%H%M%S');
mkdir -p $dir;
echo -----/etc-----
rdiff-backup -v5 /etc $dir/etc
ln -s $dir/etc/rdiff-backup-data/backup.log $dir/backup-logs/etc.log
echo -----/var-----
rdiff-backup -v5 --exclude /var/tmp --exclude /var/www --exclude /var/cache --exclude /var/crash --exclude /var/lock --exclude /var/run /var $dir/var
ln -s $dir/var/rdiff-backup-data/backup.log $dir/backup-logs/var.log
echo -----/usr-----
rdiff-backup -v5 /usr $dir/usr
ln -s $dir/usr/rdiff-backup-data/backup.log $dir/backup-logs/usr.log
echo -----/opt-----
rdiff-backup -v5 /opt $dir/opt
ln -s $dir/opt/rdiff-backup-data/backup.log $dir/backup-logs/opt.log
echo -----/srv-----
rdiff-backup -v5 /srv $dir/srv
ln -s $dir/srv/rdiff-backup-data/backup.log $dir/backup-logs/srv.log
echo -----/snap-----
rdiff-backup -v5 /snap $dir/snap
ln -s $dir/snap/rdiff-backup-data/backup.log $dir/backup-logs/snap.log
```
