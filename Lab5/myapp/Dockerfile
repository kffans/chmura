FROM nginx:alpine

COPY index.html /usr/share/nginx/html/index.html

ARG VERSION=1.0

ENV VERSION=${VERSION}

ARG HOSTNAME=webapp

ENV HOSTNAME=${HOSTNAME}

COPY version.txt /usr/share/nginx/html/version.txt

HEALTHCHECK --interval=10s --timeout=1s \
	CMD curl -f http://localhost:8080/ || exit 1

