docker pull php

docker network create laravel

docker run --name app.laravel -v .:/usr/laravel/laravel-app-crud -p 8000:8000 -w='/usr/laravel/laravel-app-crud' --network laravel -i -t -d php

docker run --detach --network laravel --name app.mariadb --env MARIADB_USER=laravel --env MARIADB_PASSWORD=laravel --env MARIADB_ROOT_PASSWORD=toor -p 3306:3306 -i -t -d mariadb:latest

mysql -h 127.0.0.1 -P 3306 -u laravel -plaravel

create database `app-crud`;

docker exec -i -t app.laravel bash

https://getcomposer.org/download/

apt-get update

apt-get install zip unzip

php composer.phar --prefer-dist --no-dev create-project laravel/laravel app-crud

php artisan serve --host 0.0.0.0

docker-php-ext-install pdo pdo_mysql

DB_CONNECTION=mysql

DB_HOST=app.mariadb

DB_PORT=3306

DB_DATABASE=app-crud

DB_USERNAME=root

DB_PASSWORD=toor

php artisan migrate

php artisan make:migation create_products_table

php artisan migrate

php artisan make:model Product

php artisan make:controller ProductController
