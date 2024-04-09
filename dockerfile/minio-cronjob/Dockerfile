FROM node:lts-alpine

USER dev

WORKDIR /app

COPY MaaRelease/scripts /app

# The `npm ci` is run before by the Github Actions

CMD ["node", "/app/minio/index.js"]
