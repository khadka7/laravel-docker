
## Laravel 10 with Docker

### Project Setup

On your local machine, clone this repo:

```bash
git clone https://github.com/khadka7/laravel-docker.git
cd laravel-docker
```

#### Docker Setup

Then build and run the documentation with [Docker Compose](https://docs.docker.com/compose/)

```bash
docker-compose up -d --build
```

> Docker Compose is included with [Docker Desktop](https://docs.docker.com/desktop/).
> If you don't have Docker Compose installed, [follow these installation instructions](https://docs.docker.com/compose/install/).

Once the container is built and running, visit [http://localhost:9000](http://localhost:9000)
in your web browser to view the docs.

To stop the staging container, use the `docker-compose down` command:

```bash
docker-compose down
```

To start the staging container again, use the `docker-compose up -d` command:

```bash
docker-compose up -d
```

##### Basic Docker commands after docker installation of docker
- You need to install dependencies in you local machine.
  ```
    docker-compose exec app composer install
    docker-compose exec app php artisan key:generate
    docker-compose exec app php artisan optimize:clear
  ```
  > In windows if `docker-compose exec` commands doesnt run in terminal or git bash try using powershell.

##### If you wish to execute command without `docker-compose exec`
- use either `docker-compose exec app sh`
- or `docker-compose exec app bash`
> then you can use commands  command without having to execute `docker-compose exec ticketing ${YOUR_COMMAND}`

##### This project is built on following docker images
- [8.1.2](https://hub.docker.com/_/php)
- [ngnix](https://hub.docker.com/_/nginx)
  
