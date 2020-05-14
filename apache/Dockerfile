# A basic apache server. To use either add or bind mount content under /var/www
#ARG BASE_IMAGE_NAME=ubuntu
#ARG BASE_IMAGE_TAG=12.04

#FROM ${BASE_IMAGE_NAME}:${BASE_IMAGE_TAG}
FROM ubuntu:12.04
#MAINTAINER Kimbro Staken version: 0.1
ARG MAIN="Kimbro Staken version: 0.1"
MAINTAINER ${MAIN}
ARG ANSH="Arg After FROM"
RUN echo ${MAIN}
RUN echo ${ANSH}
RUN apt-get update && apt-get install -y apache2 && apt-get clean && rm -rf /var/lib/apt/lists/*

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 80

CMD ["/usr/sbin/apache2", "-D", "FOREGROUND"]
