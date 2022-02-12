# Installing Apache

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

## Step 3 — Setup Firewall

<<TBD>>