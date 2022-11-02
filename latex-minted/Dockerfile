###############################################################################
FROM sfbelaine/common:latex_latest

LABEL maintainer="openscience.elaine@uni-rostock.de"

# Install texlive
RUN apt update && \
    apt install -y \
        python3-pygments && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*
