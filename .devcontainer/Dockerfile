# Use a lightweight Python base
FROM mcr.microsoft.com/vscode/devcontainers/python:3.11

# Install system dependencies
RUN apt-get update && export DEBIAN_PACKAGING_CONTROL=noninteractive \
    && apt-get -y install --no-install-recommends \
    libfontconfig1-dev \
    libgraphite2-dev \
    libharfbuzz-dev \
    libicu-dev \
    zlib1g-dev

# Install Tectonic
RUN curl --proto '=https' --tlsv1.2 -fsSL https://drop-sh.fullyjustified.net |sh
RUN mv tectonic /usr/local/bin/

# Install Pygments for the 'minted' package
RUN pip3 install Pygments
