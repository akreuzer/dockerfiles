FROM debian:stretch

MAINTAINER a_kreuzer@posteo.de

ADD https://github.com/Z3Prover/z3/releases/download/z3-4.5.0/z3-4.5.0-x64-debian-8.5.zip /z3/
RUN apt-get update \
  && apt-get install -y --no-install-recommends \
  unzip \
  libgomp1 \
  && rm -rf /var/lib/apt/lists/*

RUN cd /z3 && unzip z3-4.5.0-x64-debian-8.5.zip
RUN mv /z3/z3-4.5.0-x64-debian-8.5/bin/lib* /usr/lib \
  && mv /z3/z3-4.5.0-x64-debian-8.5/include/* /usr/include \
  && rm -rf /z3
