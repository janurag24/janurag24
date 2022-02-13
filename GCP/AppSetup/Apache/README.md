# Apache Installation Guide

## Step 1 — Installing Apache

Apache is available in default package repository.

First update local package index on local VM to reflect the latest upstream changes:

```sh
$ sudo apt update
```

Once update is done, install the apache2 package

```sh
$ sudo apt install apache2
```

## Step 2 — Check Apache Status

Once installation is completed, OS starts apache2. The web server should be running now and you can check its status by 

```sh
$ sudo systemctl status apache2
```

To check whether process is running or not
```sh
$ ps -ef | grep apache2
```

To overwrite the Apache web server default web page
```sh
$ echo '<!doctype html><html><body><h1>Hello World!</h1></body></html>' | sudo tee /var/www/html/index.html
```

## Step 3 — Setup Firewall

...

## Step 4 — Stop Apache 

To check whether process is running or not
```sh
$ ps -ef | grep apache2
```

If Apache process is running, stop the process by

```sh
$ sudo systemctl stop apache2
```

## Step 5 — Managing Apache process

To stop your web server, type:
```sh
sudo systemctl stop apache2
```

To start the web server when it is stopped, type:
```sh
sudo systemctl start apache2
```

To stop and then start the service again, type:
```sh
sudo systemctl restart apache2
```

If you are simply making configuration changes, Apache can often reload without dropping connections. To do this, use this command:
```sh
sudo systemctl reload apache2
```

By default, Apache is configured to start automatically when the server boots. If this is not what you want, disable this behavior by typing:
```sh
sudo systemctl disable apache2
```

To re-enable the service to start up at boot, type:
```sh
sudo systemctl enable apache2
```

Source - https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-debian-9

## Step 5 — Finetuning + Config Changes

### Change Listening Port

CentOS/Fedora:
```sh
$ sudo vi /etc/httpd/conf/httpd.conf
```

Ubuntu/Debian:
```sh
$ sudo vi /etc/apache2/ports.conf
```

## Step 6 — Issue Troubleshooting
