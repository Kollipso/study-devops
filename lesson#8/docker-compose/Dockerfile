FROM ubuntu:18.04

RUN apt update && apt install nginx -y

EXPOSE 80

RUN rm -rf /var/www/html/*

#VOLUME /var/www/html

CMD ["nginx", "-g", "daemon off;"]
