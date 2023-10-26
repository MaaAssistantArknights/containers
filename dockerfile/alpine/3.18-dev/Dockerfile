FROM alpine:3.18

RUN apk update --no-cache && \
    apk add --no-cache \
        build-base \
        libstdc++ \
        gcompat \
        sudo \
        bash \
        curl \
        git \
        tar \
        unzip \
        wget \
        zip && \
    adduser dev \
      --disabled-password \
      --gecos "" \
      --home "/home/dev" \
      --ingroup users \
      --shell "/bin/bash" \
      --uid "1000" && \
    mkdir -p /etc/sudoers.d && \
    echo "dev ALL=(ALL) NOPASSWD:ALL" >>/etc/sudoers.d/nopasswd

USER dev