docker pull php

docker network create laravel

docker run --name app.laravel -v .:/usr/laravel/laravel-app-crud -p 8000:8000 -w='/usr/laravel/laravel-app-crud' --network laravel  -i -t -d php

docker run --detach --network laravel --name app.mariadb --env MARIADB_USER=laravel --env MARIADB_PASSWORD=laravel --env MARIADB_ROOT_PASSWORD=toor -p 3306:3306 mariadb:latest 

docker exec -i -t app.laravel bash

https://getcomposer.org/download/

apt-get update

apt-get install zip unzip

php composer.phar --prefer-dist --no-dev create-project laravel/laravel app-crud

php artisan serve --host 0.0.0.0
