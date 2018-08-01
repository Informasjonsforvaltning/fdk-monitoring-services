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
