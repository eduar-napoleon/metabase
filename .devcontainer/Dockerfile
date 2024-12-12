# Base image with Ubuntu
FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Install Docker CLI and Docker Compose
RUN apt-get update && \
    apt-get install -y apt-transport-https ca-certificates curl software-properties-common && \
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add - && \
    add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" && \
    apt-get update && \
    apt-get install -y docker-ce-cli docker-compose

# Clean up
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

# Verify installation
RUN docker --version && docker-compose --version
