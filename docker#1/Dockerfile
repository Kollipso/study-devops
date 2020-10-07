FROM ubuntu:16.04

RUN set -ex && \
	apt update && \
	apt install -y nginx && \
	rm -rf /var/www/html/index.html

#COPY /index.html /var/www/html

VOLUME index.html /var/www/html/index.html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
