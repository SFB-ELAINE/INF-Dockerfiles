###############################################################################
FROM ubuntu:19.10

LABEL maintainer="openscience.elaine@uni-rostock.de"

# WORKDIR
WORKDIR /opt/tex

# set non interactive mode for debian
ENV DEBIAN_FRONTEND=noninteractive

# Update current instance and install texlive
RUN apt update && \
    apt full-upgrade -y && \
    apt install -y \
        git \
        texlive-full && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

CMD ["/bin/bash"]