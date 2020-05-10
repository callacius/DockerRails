FROM ubuntu:focal
MAINTAINER Daniel Costa <callacius@gmail.com>

ENV TZ 'America/Los_Angeles'

RUN echo $TZ > /etc/timezone\
 && apt-get update -y\
 && apt-get install -y tzdata\
 && rm /etc/localtime\
 && ln -snf /usr/share/zoneinfo/$TZ /etc/localtime\
 && dpkg-reconfigure -f noninteractive tzdata\
 && apt-get clean

RUN apt-get update -y\
 && apt-get upgrade -y\
 && apt-get install -y --force-yes --no-install-recommends\
	apt-utils \
     apt-transport-https \
     ssh-client \
     build-essential \
     curl \
     ca-certificates \
     git \
     libicu-dev \
     'libicu[0-9][0-9].*' \
     lsb-release \
     python-all \
     rlwrap \
 && rm -rf /var/lib/apt/lists/*;