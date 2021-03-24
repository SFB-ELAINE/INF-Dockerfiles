###############################################################################
FROM ubuntu:focal-20210217

# Installing https://github.com/richardlehane/siegfried
LABEL maintainer="openscience.elaine@uni-rostock.de"

# set non interactive mode for debian
ENV DEBIAN_FRONTEND=noninteractive

# install wget
RUN apt update && \
    apt install -y \
        wget \
        gnupg && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

RUN wget -qO - https://bintray.com/user/downloadSubjectPublicKey?username=bintray | apt-key add -

RUN echo "deb http://dl.bintray.com/siegfried/debian wheezy main" | tee -a /etc/apt/sources.list

# install siegfried
RUN apt update && \
    apt install -y \
        siegfried && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

# update signatures and build wikidata identifier
RUN sf -update && \
    roy build -wikidata

CMD ["/bin/bash"]