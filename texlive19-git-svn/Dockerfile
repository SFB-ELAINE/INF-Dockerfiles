###############################################################################
FROM debian:stable-slim

LABEL maintainer="openscience.elaine@uni-rostock.de"

# WORKDIR
WORKDIR /opt/texlive-install

# Update current instance
RUN apt update && \
    apt full-upgrade -y && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

# Install dependencies available via apt
RUN apt update && \
    apt install -y \
        wget \
        git \
        subversion \
        tex-common texinfo equivs perl-tk perl-doc \
        cm-super \
        lcdf-typetools \
        lmodern \
        t1utils \
        tex-gyre \
        texlive-font-utils \
        texlive-fonts-extra \
        texlive-fonts-extra-links \
        texlive-fonts-recommended \
        texlive-metapost && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

# Copy texlive install profile
COPY texlive.profile /opt/texlive-install/texlive.profile

# Download texlive install and run installer
RUN wget https://ftp.fau.de/ctan/systems/texlive/tlnet/install-tl-unx.tar.gz 2> /dev/null && \
    tar -xzf install-tl-unx.tar.gz && \
    cd install-tl-* && \
    ./install-tl --profile /opt/texlive-install/texlive.profile --location https://ftp.fau.de/ctan/systems/texlive/tlnet/

CMD ["/bin/bash"]