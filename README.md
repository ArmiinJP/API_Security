Welcome to the API_Security wiki!
# API_Security

for running all service:

docker-compose up


***

to see IP_ADDR using command below in terminal
> ip addr show

***


when all service run using docker-compose:

all avilable service:

1. Web console Keyclaok
     >  https://IP_ADDR:8443

2. Relying Party (for reciving key)
     >  https://IP_ADDR:1443

3. Gateway (for Calling API)
     >  https://IP_ADDR:443  or https://IP_ADDR

4. redis running port 6379

5. postgress running port 5432

6. Online Document Public api example
     >  http:IP_ADDR:7777/docs

7. Log file avilable at Logs directory

***

## Configurations:
NAME = {nginx_rp, nginx_gateway, nginx_app, keycloak, redis, postgres}

open dockers when service running:
> sudo docker exec -it NAME_proje_api bash

configure nginx service(rp, gateway, app) and reloading when running:
* /usr/local/openresty/nginx/sbin/nginx -g "daemon off;" -s reload
* nginx -g "daemon off;" -s reload

create modules with dockerfile using below command:
> sudo docker build -t NAME:latest .
