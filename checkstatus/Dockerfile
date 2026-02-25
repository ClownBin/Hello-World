FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    curl \
    git \
    jq \
    && rm -rf /var/lib/apt/lists/*

RUN curl -L -o /usr/local/bin/opencode \
    https://github.com/anomalyco/opencode/releases/latest/download/opencode-linux-x64 && \
    chmod +x /usr/local/bin/opencode

RUN opencode --version || true

ENV PATH="/root/.opencode/bin:$PATH"

WORKDIR /workspace
