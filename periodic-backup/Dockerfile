FROM alpine:latest

ARG MYSQL_ROOT_PASSWORD

COPY ./scripts/weekly/* /etc/periodic/weekly

RUN echo -e "[mysqldump]\nuser = root\npassword = $MYSQL_ROOT_PASSWORD" > /root/.my.cnf

RUN apk update && \
    apk upgrade && \
    apk add --no-cache mariadb-client && \
    chmod a+x /etc/periodic/weekly/*
