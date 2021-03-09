# Development environment
## Requirement
- [docker desktop](https://www.docker.com/get-started)
- [docker-compose](https://docs.docker.com/compose/install/)

## Setting first
Containers can connect each others wiht service name.
Normally, app service have to connect with db service - we will set ip address of db service.
For now, when we use docker-compose network, app can connect db with service name. Please set DB_HOST=db REDIS_HOST=redis in .env

## How to setup
Create src folder
> mkdir src

Clone your app to src folder
> git clone https://github.com/username/myapp.git .

## Command
Start all containers with docker-compose
> docker-compose up -d --build

Check container is running 
> docker container ls

composer command 
> docker-compose exec app composer install

php command
> docker-compose exec app php artisan migrate

yarn command
> docker-compose exec app yarn install

Remove all containers and images
> docker-compose down --rmi all
