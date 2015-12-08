############################################################
# Dockerfile to build remove_chimera FROGS tool
# Based on debian wheezy with vsearch
############################################################

# Set the base image to debian wheezy with vsearch
FROM cmonjeau/vsearch:1.9.3

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive
ENV PACKAGES python-pip perl

################## DEPENDENCIES INSTALLATION ######################

RUN apt-get update -y
RUN apt-get install -y ${PACKAGES}

######################### Clustering dep ####################################
ENV DEPS_LOC /root/remove_chimera_dep
RUN mkdir ${DEPS_LOC}
WORKDIR ${DEPS_LOC}
env PATH $PATH:${DEPS_LOC}

COPY bin/* ./
ADD remove_chimera.py .
ADD remove_chimera_tpl.html .

###############################################################

MAINTAINER Monjeaud Cyril <Cyril.Monjeaud@irisa.fr>

