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
