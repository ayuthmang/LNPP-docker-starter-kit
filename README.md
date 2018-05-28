# LNPP-docker-starter
 LNPP Stack (Nginx, PHP, Postgres) in docker

## Prerequisite

Windows requires 64bit Windows 10 Pro with Hyper-V available. Please see What to know before you install for a full list of prerequisites.

macOS & Others unix just download and install on [docker official site.](https://www.docker.com/get-docker)

## Usage

### Create and Start Containers

```
$ docker-compose up -d
```

If you already ```docker-compose up -d``` you can just

```
$ docker-compose start
```

### Stop Containers

```
$ docker-compose stop
```

### Stop and remove containers, networks, images, and volumes

```
$ docker-compose down
```

## Structures

### Overall structures

```
├── nginx
│   ├── conf    --- Nginx configuration folder
│   ├── log     --- Nginx log folder
│   └── site    --- Store our sites, php scripts
├── php7fpm
│   └── conf    --- Php fpm configuration file
└── postgresql
    ├── conf    --- PostgreSQL configuration folders
    └── data    --- PostgreSQL storage folder
```

### Private IP Address 

Private address which container talk to each others


(If you want to access with host just add uncomment in docker-compose.yml)


(If you want to edit private ip address just go to .env file)

```
LNPP_GATEWAY=172.20.1.1
LNPP_SUBNET=172.20.1.0/16

LNPP_POSTGRES_IP=172.20.1.2
LNPP_NGINX_IP=172.20.1.3
LNPP_PHP7FPM=172.20.1.4
```
