# Mise en place d'une base de données MySQL RADIUS de test
> Docker containerization of a MySQL RADIUS database for test purposes

## Installation

`
$ cp .env.example .env
`

`
$ nano .env
`

Change environment variables to suit your needs :

```text
# env

MYSQL_DATABASE=radius
MYSQL_PORT=5645
MYSQL_USER=adm-jdoe
MYSQL_PASSWORD=rootroot
MYSQL_ROOT_PASSWORD=rootroot
```

Run docker-compose :

```shell
docker-compose up -d
```

## Accessing the DB from the terminal

Access the container :

```shell
docker exec -it radius-test-database /bin/bash
```

Authenticate yourself :

```shell
mysql -u <username> -p<password>
```

Access the DB :

```shell
use radius;
```
