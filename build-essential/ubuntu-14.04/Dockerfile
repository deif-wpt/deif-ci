FROM ubuntu:14.04
MAINTAINER Esben Haabendal, eha@deif.com

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update -qq \
 && apt-get install -qq -y \
 	build-essential ssh-client git subversion curl \
	check psmisc \
	autoconf automake libtool gettext autoconf-archive pkg-config \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# /bin/sh should be bash
RUN echo "dash dash/sh boolean false" | debconf-set-selections \
 && dpkg-reconfigure dash
