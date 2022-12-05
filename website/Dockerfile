FROM alpine:latest

LABEL description = "Serve a simple website with nginx"
LABEL maintainer = "Rodet Nathan <rodetnathan.contact@gmail.com>"

RUN apk update && apk add nginx

COPY index.php /var/www/localhost/htdocs/index.php

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]

# docker build -t mon-image-nginx ./website
# docker run -p 80:80 website