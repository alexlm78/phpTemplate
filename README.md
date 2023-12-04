# PHP Develoment enviroment for Docker

Enviroment for PHP developments usign Docker

## Apache

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
