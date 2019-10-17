###############################################################################
FROM debian:stable-slim

LABEL maintainer="openscience.elaine@uni-rostock.de"

# Update current instance
RUN apt update && \
    apt full-upgrade -y && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

# Install texlive
RUN apt update && \
    apt install -y \
        texlive-full && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*
