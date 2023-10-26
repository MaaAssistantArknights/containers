FROM node:lts-alpine

USER root

# cache 优化
COPY --from=BUILD mc /root/mc

RUN apk add --no-cache git python3

COPY --from=BUILD MaaRelease/scripts /root/MaaRelease/scripts
