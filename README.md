# PHP Develoment enviroment for Docker

Enviroment for PHP developments usign Docker

## Apache

First of all, create thw ssl certificates for apache

### Create SSL certificates

```bash
mkcert -install
mkcert localhost 127.0.0.1 ::1
```

#### mkcert instalation

MacOS:

```bash
brew install mkcert
brew install nss # if you use Firefox
```

```bash
sudo port selfupdate
sudo port install mkcert
sudo port install nss # if you use Firefox
```

Linux:

```bash
sudo apt install libnss3-tools
    -or-
sudo yum install nss-tools
    -or-
sudo pacman -S nss
    -or-
sudo zypper install mozilla-nss-tools
```

### Configuring apache it self

On apache folder create 000-default.conf file

```bash
mkdir -p apache
touch apache/000-default.conf
```

For this file check the same file on this repo

### Configuring Docker

For configuring PHP on docker create the folder for this

```bash
mkdir -p php
touch php/Dockerfile
```

And check the file in this repo.

### Docker-compose

For all the proyect we have a docker compose file to acelerate the process

```bash
docker-compose -f docker-compose.apache.yml up -d  # for Apache+PHP
docker-compose -f docker-compose.nginx.yml up -d  # for Nginx+PHP
```

Beside it have a compose for Mysql to use it.

```bash
docker-compose -f docker-compose.mysql.yml up -d  # Mysql
```

### For Nginx

Just check the default.conf file and corresponging Dockerfile for this container.

Try it and let me know if you need help or if anything needs a revision.

Let's to developing.

Long live to Devs!!
