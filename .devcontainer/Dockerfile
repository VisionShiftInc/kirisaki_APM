FROM ubuntu:24.04

RUN apt-get update && apt-get install -y --no-install-recommends \
        curl \
        ca-certificates \
        git \
        python3 \
        python3-pip \
    && rm -rf /var/lib/apt/lists/*

RUN curl -sSL https://aka.ms/apm-unix | sh

WORKDIR /workspaces/kirisaki_APM
