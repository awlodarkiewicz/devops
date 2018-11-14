FROM awlodarkiewicz/devops:base

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get install -y python

# Ansible
RUN apt-get -y update
RUN apt-get -y install software-properties-common
RUN apt-add-repository -y ppa:ansible/ansible
RUN apt-get -y update
RUN apt-get -y install ansible

# Docker
RUN ansible-galaxy install geerlingguy.docker

RUN apt-get -y autoremove
