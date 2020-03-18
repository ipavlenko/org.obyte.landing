# Obyte Landing

## Clone & Install

### If PHP is configured on your host machine:

```
git clone git@github.com:ipavlenko/org.obyte.landing.git
./bin/grav install
chown -R www-data.www-data ./docroot/cache
chown -R www-data.www-data ./docroot/user
```

### If PHP is not configured on your host machine:

Configure, Build, Start, go back to this section and execute from root folder:

```
docker exec -it obyte.landing /bin/bash
```

This command shall connect you to your container. Then execute:

```
cd /var/www/html
./bin/grav install
```

Wait until the end of installation process, then exit from the container shell using command:

```
exit
```

Then execute:

```
sudo chown -R www-data.www-data ./docroot
```

## Configure

Prepare network:
```
docker network create --driver=bridge --subnet=192.168.30.0/24 obyte
```

## Build

```
yarn rebuild:obyte:landing
```

## Start

```
yarn restart:obyte:landing
```

## Network

Site IP:
192.168.30.11
