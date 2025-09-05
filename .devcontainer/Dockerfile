# Base Parrot Security image
FROM parrotsec/security:latest

# Set environment variables
ENV DEBIAN_FRONTEND=noninteractive

# Update and install essential pentest/networking tools
RUN apt-get update && apt-get install -y \
    nmap \
    net-tools \
    iproute2 \
    tcpdump \
    wireshark \
    curl \
    wget \
    git \
    python3 \
    python3-pip \
    sudo \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Set root as default user
USER root
WORKDIR /workspace
