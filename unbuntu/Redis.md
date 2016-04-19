# Redis on Ubuntu #

## 1. Installation
	$ wget http://download.redis.io/redis-stable.tar.gz
	$ tar -zxf redis-stable.tar.gz
	$ cd redis-stable
	$ make
	$ make test
	
> if tcl is required, install it by `$ apt-get install tcl`
	
	$ make install

## 2. Init redis-server
	$ wget https://github.com/ijonas/dotfiles/raw/master/etc/init.d/redis-server
	$ cp redis-server /ect/init.d
	$ chmod +x /etc/init.d/redis-server
	$ wget https://github.com/ijonas/dotfiles/raw/master/etc/redis.conf
	
> modify redis.conf, bind 127.0.0.1 and set password
	
	$ cp redis.conf /etc

### update redis configure
	$ useradd redis
	$ mkdir -p /var/lib/redis
	$ mkdir -p /var/log/redis
	$ chown redis.redis /var/lib/redis
	$ chown redis.redis /var/log/redis
	$ update-rc.d redis-server defaults

	$ /etc/init.d/redis-server start