# Place it
This repo contains the three place-it sub repo.

## Installation
1. copy .env.example as .env
## Using
to benefit from sail command you'll need to add a new alias that points to the server folder like this: `alias sail2='sh $([ -f sail ] && echo sail || echo place-it-server/vendor/bin/sail)'`

## urls
server
```
http://server.place-it.test
```
client
```
http://place-it.test
```

## testing
You'll need to create a database `larave_test` and gant it appropriate permissions

1. copy .env.dusk.local.example as .env.dusk.local