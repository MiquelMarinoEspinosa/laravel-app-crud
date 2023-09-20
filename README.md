docker pull php

docker run --name app.laravel -v .:/usr/laravel -p 80:80 -w='/usr/laravel' -d -i -t php

docker exec -i -t app.laravel bash

https://getcomposer.org/download/

apt-get update

apt-get install zip unzip

php composer.phar --prefer-dist --no-dev create-project laravel/laravel app-crud
