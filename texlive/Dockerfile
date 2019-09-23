FROM ubuntu:latest

LABEL maintainer="gregunz <mail@gregunz.io>"

ENV LANG=C.UTF-8
ENV DEBIAN_FRONTEND=noninteractive

## install texlive-full
RUN apt update && \
    apt install -y texlive-full

## cleaning
RUN apt clean && \
    apt autoremove

RUN rm -rf \
      /var/lib/apt/lists/* \
      /tmp/* \
      /var/tmp/*

WORKDIR /opt/app

ENTRYPOINT [ "pdflatex" ]
