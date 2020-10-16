# deploy

docker network create --driver overlay traefik_endpoint

DOMAIN_NAME='mylocal.mylocal' docker stack deploy -c docker-compose.yml $(basename $PWD)
