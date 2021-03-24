###############################################################################
FROM sfbelaine/common:texlive19-git_latest

LABEL maintainer="openscience.elaine@uni-rostock.de"

# Install svn
RUN apt update && \
    apt install -y \
        subversion && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*
