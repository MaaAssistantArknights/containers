FROM node:lts-alpine

USER root

# cache 优化
COPY mc /root/mc

RUN apk add --no-cache git python3

COPY MaaRelease/scripts /root/MaaRelease/scripts
