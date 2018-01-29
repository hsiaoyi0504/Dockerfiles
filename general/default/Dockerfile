FROM ubuntu:16.04
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
&& apt-get install -y apt-utils \
&& apt-get -y upgrade \
&& apt-get install -y build-essential \
&& apt-get install -y git-all \
&& apt-get install -y iputils-ping \
&& apt-get install -y wget \
&& apt-get install -y vim