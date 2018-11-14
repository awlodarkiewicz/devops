FROM ubuntu:18.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install -y aptitude software-properties-common
RUN apt-get install -y curl git gettext-base

RUN apt-get -y autoremove
