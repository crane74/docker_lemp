FROM mcr.microsoft.com/devcontainers/php:0-8.2

RUN apt update && apt upgrade -y  \
    && apt install -y default-mysql-client  \
    && apt clean \
    && rm -rf /var/lib/apt/lists/*

USER vscode

# starshipの導入
RUN curl -sS https://starship.rs/install.sh | sh -s -- --yes && \
    echo eval "$(starship init bash)" >> ~/.bashrc



