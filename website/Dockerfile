FROM ubuntu:20.04

ENV DEBIAN_FRONTEND noninteractive

LABEL description = "Serve a simple website with apache2"
LABEL maintainer = "Rodet Nathan <rodetnathan.contact@gmail.com>"

RUN apt-get update && apt-get install -y apache2
RUN mkdir -p /var/www/html

COPY index.php /var/www/html/

ENV PASSWORD=toto
ENV USERNAME=python

EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND"]

# docker build -t website ./website
# docker run --name website -p 80:80 website

# Pas à jour