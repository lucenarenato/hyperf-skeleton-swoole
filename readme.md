mkdir hyperf-skeleton && cd hyperf-skeleton
docker run -v ${PWD}:/app -p 9501:9501 -it --entrypoint /bin/sh hyperf/hyperf:8.0-alpine-v3.13-swoole
composer create-project hyperf/hyperf-skeleton app
docker compose run --rm --service-ports hyperf-skeleton
php bin/hyperf.php start
