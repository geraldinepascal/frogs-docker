############################################################
# Dockerfile to build container images
# Based on debian
# Tool on FROGS applications 
# https://github.com/geraldinepascal/FROGS
############################################################

# Set the base image to Ubuntu
FROM debian:wheezy

# File Author / Maintainer
MAINTAINER Sandrine Perrin <sandrine.perrin@france-bioinformatique.fr>

# Set environment variable
ENV TOOL_NAME clusters_stat 
ENV TOOL_VERSION 1.4.0
ENV TOOL_PKG ${TOOL_ID}_v${TOOL_VERSION}.zip

ENV PACKAGES python=2.7.3-4+deb7u1 perl=5.14.2-21+deb7u2 python-numpy=1:1.6.2-1.2 python-scipy=0.10.1+dfsg2-1

# Update the repository sources list
RUN apt-get update

# Install dependency
RUN apt-get install --yes $PACKAGES

# Download internal dependencies
COPY bin/* /usr/local/bin/

# Install tool
COPY clusters_stat* /usr/local/bin/
RUN chmod +x /usr/local/bin/*

# Cleanup
RUN apt-get clean
# Set entrypoint
