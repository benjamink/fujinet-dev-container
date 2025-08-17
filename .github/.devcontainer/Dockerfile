FROM mcr.microsoft.com/devcontainers/base:${VARIANT:-bullseye}

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get -y install --no-install-recommends \
        curl \
        ca-certificates \
        apt-transport-https \
        gnupg2 \
        lsb-release \
        software-properties-common \
        build-essential \
        flex \
        git \
        unzip \
        bison \
    && rm -rf /var/lib/apt/lists/*

# Install cc65
RUN <<EOF
  set -e
  cd /tmp
  git clone https://github.com/cc65/cc65.git
  cd cc65
  export PREFIX=/usr/local
  make
  make install
  cd /tmp
  rm -rf cc65*
EOF