FROM rocker/rstudio

MAINTAINER vinicius.remigio@gmail.com

# Variables

ENV SPARK_VERSION 1.6.0
ENV HADOOP_VERSION 2.6

# Update Ubuntu

RUN apt-get update \
    && apt-get install -y software-properties-common debconf-utils \
    && add-apt-repository ppa:webupd8team/java \
    && apt-get update

# Install java

RUN echo "oracle-java8-installer shared/accepted-oracle-license-v1-1 select true" | debconf-set-selections \ 
    && apt-get install -y oracle-java8-installer oracle-java8-set-default

# Install rJava

RUN apt-get install r-cran-rjava \
 	 && R CMD javareconf

# Install SparkR (Spark > 1.4.1)

RUN wget -O /tmp/spark.tgz http://mirror.nbtelecom.com.br/apache/spark/spark-$SPARK_VERSION/spark-$SPARK_VERSION-bin-hadoop$HADOOP_VERSION.tgz \
	&& tar -xf /tmp/spark.tgz -C /opt/

RUN ln -s /opt/spark-$SPARK_VERSION-bin-hadoop$HADOOP_VERSION /opt/spark

# Install R packages at Docker Image build time

ADD resources/setup.R /tmp/setup.R

RUN Rscript --vanilla /tmp/setup.R




