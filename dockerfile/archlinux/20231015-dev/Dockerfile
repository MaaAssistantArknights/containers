FROM archlinux:base-20231015.0.185077

RUN pacman -Syu --noconfirm && \
    pacman -S --noconfirm \
    base-devel \
    python3 \
    python-pip \
    curl \
    wget \
    git \
    sudo && \
    pacman -Scc --noconfirm && \
    useradd dev \
      --create-home \
      --shell=/bin/bash \
      --uid=1000 \
      --user-group && \
    mkdir -p /etc/sudoers.d && \
    echo "dev ALL=(ALL) NOPASSWD:ALL" >>/etc/sudoers.d/nopasswd

USER dev