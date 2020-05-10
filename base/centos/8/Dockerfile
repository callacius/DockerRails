FROM centos:8
MAINTAINER Daniel Costa <callacius@gmail.com>

RUN dnf -y update && dnf clean all

RUN sudo dnf install -y \
  https://download1.rpmfusion.org/free/el/rpmfusion-free-release-$(rpm -E %el).noarch.rpm
  
RUN sudo dnf install -y \
  https://download1.rpmfusion.org/nonfree/el/rpmfusion-nonfree-release-$(rpm -E %el).noarch.rpm
  
RUN sudo dnf module list nodejs

RUN dnf install -y \
      automake \
      libicu \
      curl \
      gcc \
      gcc-c++ \
      git \
      kernel-devel \
      make \
      perl \
      python \
      which \
 && dnf clean all

