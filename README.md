# Pré-requis
- [Docker](https://docs.docker.com/get-docker/)
- Composer


```dockerfile
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
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
