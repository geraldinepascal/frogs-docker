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
ENV TOOL_NAME affiliations_stat 
ENV TOOL_VERSION 1.1.0

ENV PACKAGES python2.7-minimal apt-utils

# Update the repository sources list
RUN apt-get update

# Install dependency
RUN apt-get install --yes $PACKAGES

# Download internal dependencies
COPY bin/* /usr/local/bin/

# Install tool
COPY affiliations_stat* /usr/local/bin/
RUN chmod +x /usr/local/bin/*


# Cleanup
RUN apt-get clean
