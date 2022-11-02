###############################################################################
FROM ubuntu:focal-20221019

LABEL maintainer="openscience.elaine@uni-rostock.de"

# WORKDIR
WORKDIR /opt/tex

# set non interactive mode for debian
ENV DEBIAN_FRONTEND=noninteractive

# Update current instance and install texlive
RUN apt update && \
    apt install -y \
        git \
        texlive-full && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

CMD ["/bin/bash"]