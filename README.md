# Reverse proxy nginx

Setup for nginx reverse proxy redirecting to nodejs app and pgadmin service connected to PostgreSQL. All the apps are dockerized and compose in the docker-compose file. 

## Prerequisites
- Docker 
- Docker compose 

## Services.
- Nodejs - port 8502
- PostgreSQL - port 81
- PGadmin - port 5050
- NGINX - port 80

## Discription

In the /nginx/reverse-proxy file I used 7test.com and pg.test.com for Node and Pgadmin respectively. You can castomize it to whatever you'd like. For it change 
`server_name = 7test.com`
to 
`server_name = your-example.com `

and add 
`127.0.0.2 example1.com`
`127.0.0.3 example2.com`

to `/etc/hosts` file on Linux or 
`C:\Windows\System32\drivers\etc\Hosts` on Windows 

## Start 

After setting URLs up, run 

``docker compose up -d``

to pull everything from hub and start containers.