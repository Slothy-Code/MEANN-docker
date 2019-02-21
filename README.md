# Angular 2, Express and Docker Compose project starter

## Getting started

    $ git clone https://github.com/Slothy-Code/MEANN-docker.git my-project

## Development

     docker-compose build

After successfully:
    
     docker-compose up -d

The following services will be available:

* Angular 2 webapp - http://localhost:4200
* Express webapp - http://localhost:3000

### Angular 2

This is built with [Angular CLI](https://github.com/angular/angular-cli) version 7.3.1. It runs `ng serve` command to start in development mode with livereload. 
A volume is linked to the `client/src` directory for local development.

### Express

This runs using `nodemon` to provide livereload. A volume is link to the `express/routes` directory for local development.

## Production

    $ docker-compose -f docker-compose-prod.yml up -d

All services are locked down except for the express webapp running on port 80.
