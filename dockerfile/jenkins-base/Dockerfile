FROM node:lts-alpine

USER root

WORKDIR /root

COPY mc /root/mc

COPY MaaRelease/scripts /root/MaaRelease/scripts

RUN apk add --no-cache git python3
