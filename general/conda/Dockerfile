FROM ubuntu:16.04
ARG DEBIAN_FRONTEND=noninteractive
RUN rm /bin/sh && ln -s /bin/bash /bin/sh
RUN apt-get update
RUN apt-get install -y apt-utils
RUN apt-get -y upgrade
RUN apt-get install -y build-essential
RUN apt-get install -y git-all
RUN apt-get install -y iputils-ping
RUN apt-get install -y wget
RUN apt-get install -y vim
RUN wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda.sh
RUN bash miniconda.sh -b -p $HOME/miniconda
ENV PATH /root/miniconda/bin:$PATH
RUN hash -r
RUN conda config --set always_yes yes --set changeps1 no
RUN conda update -q conda
RUN conda install -q conda-build
RUN conda update -q conda-build
RUN conda config --add channels conda-forge