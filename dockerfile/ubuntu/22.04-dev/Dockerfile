FROM ubuntu:22.04

FROM ubuntu:22.04

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y \
    curl \
    wget \
    sudo \
    build-essential \
    python3 \
    python3-pip \
    vim && \
    useradd dev \
      --create-home \
      --shell=/bin/bash \
      --uid=1000 \
      --user-group && \
    mkdir -p /etc/sudoers.d && \
    echo "dev ALL=(ALL) NOPASSWD:ALL" >>/etc/sudoers.d/nopasswd

USER dev
