FROM ubuntu:18.04

USER root

RUN mkdir -p /work/
RUN mkdir -p /data/

RUN apt-get update && apt-get install -y \
    git \
    python3-pip \
    python3-dev

RUN pip3 install --upgrade pip
RUN pip3 install --upgrade setuptools

# copy requirements.txt to container and install
COPY requirements.txt /work/requirements.txt
COPY ./ /work

WORKDIR /work/

RUN pip3 install -r /work/requirements.txt
