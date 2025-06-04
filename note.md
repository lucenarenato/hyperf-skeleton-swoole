mkdir hyperf-skeleton && cd hyperf-skeleton
docker run -v ${PWD}:/app -p 9501:9501 -it --entrypoint /bin/sh hyperf/hyperf:8.0-alpine-v3.13-swoole
composer create-project hyperf/hyperf-skeleton app
composer install --ignore-platform-req=ext-swoole

docker compose run --rm --service-ports hyperf-skeleton
php bin/hyperf.php start


## dockerfile image 
    image: hyperf/hyperf:8.0-alpine-v3.13-swoole

- https://rlucena.com/post/hyperf-php-coroutine-framework-baseado-em-swoole