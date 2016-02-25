FROM rocker/rstudio

MAINTAINER vinicius.remigio@gmail.com

# Setup Ubuntu

RUN apt-get update \
    && apt-get install -y software-properties-common debconf-utils \
    && add-apt-repository ppa:webupd8team/java \
    && apt-get update

# Install java

RUN echo "oracle-java8-installer shared/accepted-oracle-license-v1-1 select true" | debconf-set-selections \ 
    && apt-get install -y oracle-java8-installer oracle-java8-set-default \
    && java -version
