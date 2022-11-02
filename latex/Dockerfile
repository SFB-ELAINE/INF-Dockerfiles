###############################################################################
FROM debian:stable-20221024-slim

LABEL maintainer="openscience.elaine@uni-rostock.de"

# Install texlive
RUN apt update && \
    apt install -y \
        texlive-full && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*
