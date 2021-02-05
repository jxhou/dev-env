## Dev environment
 
This dev environment includes following containers:
- nginx: a reverse proxy for all the microservices hosted in the dev environment.
- a client server: serves as angular app server.
- an API server: serves as an application api server.
- postgres DB: a postgres database server as a backend of api server.
- pgadmin: serves a web UI for monotoring the postgres database.

Clone this repository and 
ContentExplorer [https://github.com/jxhou/ContentExplorer]: an angular project'
api-server [https://github.com/jxhou/api-server]: a backend server

run docker-compose up in docker environment such as wsl in windows 10, which should spin up all the containers.

goto localhost:3050 in browser, should see an Angular frontend.
Currently only login page is connected to backend.

## postgres and pgamdin

### Environments
This Compose file contains the following environment variables:

- POSTGRES_USER the default value is postgres
- POSTGRES_PASSWORD the default value is postgres
- PGADMIN_PORT the default value is 5050
- PGADMIN_DEFAULT_EMAIL the default value is pgadmin4@pgadmin.org
- PGADMIN_DEFAULT_PASSWORD the default value is admin

### Access to postgres:
- localhost:5432
- Username: postgres (as a default)
- Password: postgres (as a default)

### Access to PgAdmin:
- URL: http://localhost:5050
- Username: pgadmin4@pgadmin.org (as a default)
- Password: admin (as a default)

### Add a new server in PgAdmin:
- Host name/address postgres
- Port 5432
- Username as POSTGRES_USER, by default: postgres
- Password as POSTGRES_PASSWORD, by default postgres

### References
[Postgresql & PgAdmin powered by compose](https://github.com/khezen/compose-postgres)