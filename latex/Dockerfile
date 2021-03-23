###############################################################################
FROM debian:stable-20210311-slim

LABEL maintainer="openscience.elaine@uni-rostock.de"

# Install texlive
RUN apt update && \
    apt install -y \
        texlive-full && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*
