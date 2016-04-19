# Nodejs on Ubuntu

## 1. Install NVM

	$ wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh | bash
	$ . ~/.nvm/nvm.sh
	
## 2. Install Node & NPM

	$ nvm install 4.2
	$ nvm use 4.2
	$ node -v
	$ npm -v
	
## 3. Config CNPM
update .bashrc: `$ vim ~/.bashrc`

	alias cnpm="npm --registry=https://registry.npm.taobao.org \
		--cache=$HOME/.npm/.cache/cnpm \
		--disturl=https://npm.taobao.org/dist \
		--userconfig=$HOME/.cnpmrc"