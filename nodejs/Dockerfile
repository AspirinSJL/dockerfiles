FROM ubuntu:14.04

RUN apt-get update -y && apt-get install --no-install-recommends -y -q curl python build-essential git ca-certificates
RUN mkdir /nodejs && curl http://npm.taobao.org/mirrors/node/latest/node-v0.12.3-linux-x64.tar.gz | tar xvzf - -C /nodejs --strip-components=1

ENV PATH $PATH:/nodejs/bin

RUN npm install -g cnpm --registry=https://registry.npm.taobao.org