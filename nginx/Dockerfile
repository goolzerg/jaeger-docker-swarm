FROM nginx:latest

RUN apt-get update && \
apt-get install -y curl 

COPY default.conf /etc/nginx/conf.d
