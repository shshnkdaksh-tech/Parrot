# Use the Parrot Security Core base image
FROM parrotsec/core:latest

# Install basic tools
RUN apt update && apt install -y \
    git \
    curl \
    vim \
    python3 \
    python3-pip \
    net-tools \
    sudo \
    nmap \
    hydra \
    john \
    && rm -rf /var/lib/apt/lists/*

# Set bash as default shell
SHELL ["/bin/bash", "-c"]

# Create a non-root user for Codespaces
RUN useradd -m codespace && echo "codespace ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
USER codespace
WORKDIR /home/codespace
