FROM nginx:latest

LABEL maintainer="Ye Htet Aung <yehtetag.y@gmail.com>"

COPY ./configure-api.sh /docker-entrypoint.d/
COPY resources /usr/share/nginx/html/resources
COPY ./index.html /usr/share/nginx/html/


 
