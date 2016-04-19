# FTP on Ubuntu #

## 1. Installation & configuration ##

	$ apt-get install vsftpd

edit vsftpd.conf: `$ vim /etc/vsftpd.conf`
  
	anonymous_enable=NO
	local_enable=YES
	local_write=YES

restart service

	$ service vsftpd restart

## 2. Config user ##
	$ adduser myProject -d /home/myProject
	$ passwd myProject
 	$ cd /home
 	$ chown -R myProject ./myProject
	$ chmod 775 ./myProject