# step dy step

# Удалить все контейнеры
docker rm -f $(docker ps -a -q)

# Удалить все имиджи
docker rmi -f $(docker images -q)

# Dockerfile
FROM ubuntu:18.04

RUN apt update && apt install nginx -y

EXPOSE 80

RUN rm -rf /var/www/html/*

VOLUME /var/www/html

CMD ["nginx", "-g", "daemon off;"]

# create index.html
vim index.html

# build image
docker build -t web1 .

# run container
docker run -d -p 8080:80 -v /home/user/study/test01:/var/www/html web1

# check nginx
curl localhost:8080

# edit index.html
vim index.html

# check nginx
curl localhost:8080

# install docker
