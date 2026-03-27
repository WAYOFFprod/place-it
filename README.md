# Place it

This repo contains the three place-it sub repo.

## Installation

1. copy .env.example as .env

## Starting

launch all the containers using

```bash
# Dev
docker compose -f docker-compose.yml -f docker-compose.dev.yml up # --build if you need to rebuild

# Preview
docker compose -f docker-compose.yml -f docker-compose.preview.yml up --build
```

if it is the first time you'll need to run the migration on the server with the seeder

```bash
php artisan migrate:fresh -seed
```

and generate a token for the websocket server

```bash
php artisan app:create-token
```

copy the output and put it in the .env that is above the 3 projects (same level as this readme)

## Using

to benefit from sail command you'll need to add a new alias that points to the server folder like this: `alias sail2='sh $([ -f sail ] && echo sail || echo place-it-server/vendor/bin/sail)'`

## urls

server

```
http://server.place-it.test
```

client

```
http://place-it.test:5173/
```

## testing

You'll need to create a database `larave_test` and gant it appropriate permissions

1. copy .env.dusk.local.example as .env.dusk.local
