############################################################
# Dockerfile to build container images
# Based on debian
# Tool on FROGS applications 
# https://github.com/geraldinepascal/FROGS
############################################################

# Set the base image to Ubuntu
FROM debian:wheezy

# File Author / Maintainer
MAINTAINER Yvan Le Bras <yvan.le_bras@irisa.fr>

# Set environment variable
ENV TOOL_NAME normalisation 
ENV TOOL_VERSION 0.6.0
ENV TOOL_PKG ${TOOL_ID}_v${TOOL_VERSION}.zip

ENV PACKAGES python2.7-minimal apt-utils

# Update the repository sources list
RUN apt-get update

# Install dependency
RUN apt-get install --yes $PACKAGES

# Download internal dependencies
COPY bin/* /usr/local/bin/

# Install tool
COPY normalisation.py /usr/local/bin/
RUN chmod +x /usr/local/bin/*

# Cleanup
RUN apt-get clean