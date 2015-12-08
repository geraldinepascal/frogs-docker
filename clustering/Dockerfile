############################################################
# Dockerfile to build clustering FROGS tool
# Based on debian wheezy with Swarm
############################################################

# Set the base image to debian wheezy with swarm
FROM cmonjeau/swarm:2.1.5

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive
ENV PACKAGES python-pip perl

################## DEPENDENCIES INSTALLATION ######################

RUN apt-get update -y
RUN apt-get install -y ${PACKAGES}

######################### Clustering dep ####################################
ENV DEPS_LOC /root/clustering_dep
RUN mkdir ${DEPS_LOC}
WORKDIR ${DEPS_LOC}
env PATH $PATH:${DEPS_LOC}

COPY bin/* ./
ADD clustering.py .

###############################################################

MAINTAINER Monjeaud Cyril <Cyril.Monjeaud@irisa.fr>

