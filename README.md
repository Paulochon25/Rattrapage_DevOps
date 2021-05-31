# Pré-requis
- [Docker](https://docs.docker.com/get-docker/)
- Composer


```bash
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
#Installer Memcached

To install this extension, SSH in to your server as root and run the following commands:

```bash
$ sudo apt-get -y install gcc make autoconf libc-dev pkg-config
$ sudo apt-get -y install zlib1g-dev
$ sudo apt-get -y install libmemcached-dev
$ sudo pecl5.X-sp install memcached-2.2.0
```
When you are shown the prompt
```bash
$ libmemcached directory [no] :
```
type or paste the following text exactly as shown and press Enter.

```bash
$ no --disable-memcached-sasl
```

That is, the entire line you'll see on your screen will be as follows once you press Enter.
```bash
$ libmemcached directory [no] : no --disable-memcached-sasl
```

Once installed, create a configuration file for the extension and restart PHP by running the following commands as root

```bash
$ sudo bash -c "echo extension=memcached.so > /etc/php5.X-sp/conf.d/memcached.ini"
$ sudo service php5.X-fpm-sp restart
```


# Set-up

A la racine du répertoire, déplacez vous dans le dossier wordpress-compose
```bash
$ cd wordpress-compose
```

Ensuite nous allons exécuter `docker-compose.yml` pour créer nos containers

```bash
$ docker-compose up -d
```

Une fois les conteneurs lancés, votre site WordPress est en place !

Il ne restera qu'à le configurer en y accédant depuis votre navigateur, à l'adresse`localhost`
