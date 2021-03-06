# Nextcloud setup

To setup nextcloud with this configuration, you will have to also install the `traefik-docker` project available [here](https://github.com/m1rkwood/traefik-docker).

## Folder structure

```
app/
.env
docker-compose.yml
Dockerfile
```

## Envionment

Duplicate the `.env.template` and rename it to `.env`
In the `.env` file, add below information.

```
NEXTCLOUD_ROOT=<DIRECTORY>/app
MYSQL_ROOT_PASSWORD=
MYSQL_PASSWORD=
REDIS_PASSWORD=
SUB_DOMAIN=
DOMAIN_NAME=
```

For `NEXTCLOUD_ROOT`, navigate to your desired folder, and type `pwd` to know its absolute path. Any path will do, as an example, `/home/nextcloud` or `/root/nextcloud` will both work. For the passwords, generate strong passwords.

`NEXTCLOUD_HOST` is the domain used, i.e. `cloud.domain.com`

## Build the image & start the containers

Builds the containers from the `docker-compose.yml` and `Dockerfile`
Always run these commands from the main folder that contains your `docker-compose.yml` file

```
docker-compose build
docker-compose up -d
```
