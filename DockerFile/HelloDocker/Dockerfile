FROM nginx:latest

LABEL maintainer="Ömer Taha Öztop"
LABEL version="1.0"
LABEL name="hello-docker"

ENV KULLANICI="omertahaoztop"

RUN apt-get update
RUN apt-get install curl -y
WORKDIR /usr/share/nginx/html
COPY hello_docker.html /usr/share/nginx/html
HEALTHCHECK --interval=30s --timeout=10s --start-period=5s --retries=3 CMD curl -f http://localhost/ || exit 1
CMD sed -e s/Kullanici/"$KULLANICI"/ Hello_docker.html > index1.html && sed -e s/Hostname/"$HOSTNAME"/ index1.html > index.html ; rm index1.html Hello_docker.html; nginx -g 'daemon off;'