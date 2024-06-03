# Docker Compose for PHP Application

This is a project template for PHP 8.3 projects. It's recommended for local development purposes only.

The Docker image is based on `php:8.3-apache` official image on Docker hub plus _Composer_ and below PHP extensions:
- opcache
- pdo_mysql
- decimal
- xdebug

## Get Started
```shell
cp .env.example.dc .env
```

You can customize the values of environment variables based on your specific needs, especially port numbers
to prevent potential port conflicts.

```shell
docker compose up -d
```

There is a `src` folder that is designed for you to put your application source code in it, whether it's a Laravel app
or just vanilla PHP. Just notice that the `src/public` directory will be used as the **document root** by Apache.

## Laravel
A Laravel 11 template project is created in the `src` folder. To make use of it, you need to run the below commands:

```shell
docker compose exec php bash

# run below commands inside the container
cp .env.example .env
composer install
```
