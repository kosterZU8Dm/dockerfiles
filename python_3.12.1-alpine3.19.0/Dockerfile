# syntax=docker/dockerfile:1
FROM alpine:3.19.0 as build
LABEL maintainer="kostochka11@proton.me"

ARG BUILD_SPACE=/var/build_space
ARG PYTHON_VERSION=3.12.1
USER root
RUN apk update \
  && apk add build-base zlib-dev openssl-dev libffi-dev\
  && mkdir -p $BUILD_SPACE
WORKDIR $BUILD_SPACE
RUN wget https://www.python.org/ftp/python/$PYTHON_VERSION/Python-$PYTHON_VERSION.tgz \
  && tar -xvzf Python-$PYTHON_VERSION.tgz \
  && cd Python-$PYTHON_VERSION \
  && ./configure \
  && make \
  && make install
