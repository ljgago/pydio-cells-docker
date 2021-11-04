FROM alpine:latest

COPY ./scripts/weekly/* /etc/periodic/weekly

RUN apk update && \
    apk upgrade && \
    apk add --no-cache mariadb-client && \
    chmod a+x /etc/periodic/weekly/*
