############################################################
# Dockerfile to build FROGS affiliation_OTU deps
# Based on debian wheezy with RDPTools
############################################################

# Set the base image to debian wheezy with flash
FROM cmonjeau/rdptools

# Set noninterative mode
ENV DEBIAN_FRONTEND noninteractive
ENV PACKAGES perl util-linux ncbi-blast+

################## DEPENDENCIES INSTALLATION ######################

RUN apt-get update -y
RUN apt-get install -y ${PACKAGES}

################## AFFILIATION_OTU DEPENDENCIES ######################

WORKDIR /root/affiliation_otu_deps
ENV PATH $PATH:/root/affiliation_otu_deps/

COPY bin/* /usr/local/bin/
COPY affiliation_* /usr/local/bin/
RUN chmod +x /usr/local/bin/*


RUN cp -r /opt/RDPTools/* ./

###############################################################

MAINTAINER Monjeaud Cyril <Cyril.Monjeaud@irisa.fr>
