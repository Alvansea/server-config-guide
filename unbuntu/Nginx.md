# Nginx on Ubuntu

## 1. Installation
	$ apt-get update
	$ apt-get install nginx
	$ /etc/init.d/nginx start
	
## 2. Configuration
Create site config file: 

	$ vim /etc/nginx/sites-enabled/mySite
	
Edit config: 
	
	server {
        listen          80;
        server_name     www.mydomain.com;
        location / {
        	proxy_pass      http://localhost:8080;
        }
	}

Restart nginx: 
	
	$ /etc/init.d/nginx restart