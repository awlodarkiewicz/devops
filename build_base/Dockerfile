FROM ubuntu:18.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get -qq -y upgrade && \
    apt-get -qq -y --no-install-recommends install \
        software-properties-common curl git gettext-base && \
    apt-get -y autoremove && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
