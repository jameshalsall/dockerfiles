FROM quay.io/continuouspipe/ubuntu16.04:latest

MAINTAINER Kieren Evans <kieren.evans+cp-dockerfiles@inviqa.com>

RUN curl -q https://dx6pc3giz7k1r.cloudfront.net/GPG-KEY-inviqa-tools | apt-key add - \
 && echo "deb https://dx6pc3giz7k1r.cloudfront.net/repos/debian jessie main" | tee /etc/apt/sources.list.d/inviqa-tools.list \
 && apt-get update -qq \
 && apt-get -qq -y --no-install-recommends install \
    hem \
 \
 # Clean the image \
 && apt-get auto-remove -qq -y \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*
