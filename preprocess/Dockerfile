############################################################
# Dockerfile to build FROGS preprocess deps
# Based on debian wheezy with flash
############################################################

# Set the base image to debian wheezy with flash
FROM cmonjeau/flash:1.2.11

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive
ENV PACKAGES python-pip perl git

################## DEPENDENCIES INSTALLATION ######################

RUN apt-get update -y
RUN apt-get install -y ${PACKAGES}

#################### CUTADAPT INSTALLATION #####################

RUN pip install cutadapt

######################### FROGS DEP ####################################

RUN mkdir preprocess_dep
WORKDIR preprocess_dep
env PATH $PATH:/root/preprocess_dep/

COPY bin/* ./
ADD preprocess.py .
ADD preprocess_tpl.html .

###############################################################

MAINTAINER Monjeaud Cyril <Cyril.Monjeaud@irisa.fr>

