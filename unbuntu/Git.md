# Git on Ubuntu #

## 1. Install git-core ##
	$ apt-get install git-core

## 2. Configure user and group ##
	$ groupadd developers
	$ cd /home
	$ mkdir git
	$ useradd git -d /home/git
	$ passwd git

modify /etc/group, add git to developers group: `$ vim /etc/group`
  
	developers:x:1000:git
		
## 3. Init repository ##
create repo folder

	$ cd /home/git
	$ mkdir myProject.git
	
config access permissions

	$ chgrp -R developers myProject.git
	$ chmod -R g+rws myProject.git

initialize repo

	$ git init --bare --shared myProject.git