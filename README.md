# Monitoring

!!! WORK IN PROGRESS !!!

This is an experimental project to explore monitoring stacks:
* the TIG-stack (Telegraf, InfluxDB and Grafana)
* the TICK-stack (Telegraf, InfluxDB, Chronograf and Kapacitor)

The service being monitored is a simple example-api: https://hub.docker.com/r/informasjonsforvaltning/example-api/

## TIG-stack
Usage:
```
docker-compose -f docker-compose_TIG.yml up -d
```
Open localhost:3000 in your browser. Username/password: admin/admin

## TICK-stack
Usage:
```
docker-compose -f docker-compose_TICK.yml up -d
```
Open localhost:8888 in your browser.

## Generating load
An easy way to generate load to the example-api could be done with [loadtest](https://github.com/alexfernandez/loadtest)
```
npm install -g loadtest
loadtest  -c 2 --rps 1 -k http://localhost:8080/pets
loadtest  -c 2 --rps 1 -k -P '{"name": "test", "species": "testSpecie"}' -T 'application/json' -m POST http://localhost:8080/pets # in another bash-shell
```
