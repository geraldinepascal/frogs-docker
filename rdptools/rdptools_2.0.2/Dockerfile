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
ENV TOOL_NAME RDPTools
ENV TOOL_ID rdptools
ENV TOOL_VERSION 2.0.2

ENV PACKAGES \
        ant \
        git \
        make \
        ncbi-blast+=2.2.26-3 \
        python=2.7.3-4+deb7u1 \
        openjdk-7-jdk \
        openjdk-7-jre-headless

ENV JAVA_HOME /usr/lib/jvm/java-7-openjdk-amd64

# Update the repository sources list
RUN apt-get update

# Install dependency
RUN apt-get install --yes $PACKAGES

# Download internal dependencies
WORKDIR /tmp
RUN git clone https://github.com/rdpstaff/RDPTools.git && \
    cd ${TOOL_NAME}* && \
    git checkout $TOOL_VERSION && \
    git submodule update --init && \
    make  && \
    cp *.jar /usr/local/bin/

# Copy dependencies for RDPTools
RUN cp -r ${TOOL_NAME}*/lib /usr/local/bin/

# Make script executable
RUN chmod +x /usr/local/bin/*

# Cleanup
RUN apt-get clean
RUN rm -r ${TOOL_NAME}*
WORKDIR /

# Set entrypoint

