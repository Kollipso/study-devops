# deploy

DOMAIN_NAME='mylocal.mylocal' docker stack deploy -c docker-compose.yml $(basename $PWD)
