FROM ubuntu:14.04

RUN apt-get update

RUN apt-get install -y python3-pip python3-dev g++ libopenblas-dev libblas-dev liblapack-dev libatlas-base-dev gfortran

# ML Pipeline packages
RUN pip3 install numpy scipy pandas sklearn jupyter  

# TensorFlow
RUN export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-0.10.0rc0-cp34-cp34m-linux_x86_64.whl && pip3 install --upgrade $TF_BINARY_URL

# Theano
RUN pip3 install theano 

# Keras
RUN apt-get install -y libhdf5-dev && \
	pip3 install pyyaml h5py keras