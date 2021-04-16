# FDK Monitoring Services (TIG)

## TIG-stack
Usage:
```
docker-compose -f docker-compose.yml up -d
```
Open localhost:3000 in your browser. Username/password: admin/admin

## Statsd
Telegraf uses statsd (UDP port 8125) to collect metrics from services. 

### Spring Boot
With Spring Boot Actuator + Micrometer Statsd it is very easy to collect metrics and submit these using statsd.
