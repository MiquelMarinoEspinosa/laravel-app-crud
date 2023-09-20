docker pull php

docker run --name app.laravel -v .:/usr/laravel/laravel-app-crud -p 8000:8000 -w='/usr/laravel/laravel-app-crud' --network php8_default  -i -t -d php

docker exec -i -t app.laravel bash

https://getcomposer.org/download/

apt-get update

apt-get install zip unzip

php composer.phar --prefer-dist --no-dev create-project laravel/laravel app-crud

php artisan serve --host 0.0.0.0
