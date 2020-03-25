FROM ubuntu:18.04

ENV node_version v12.16.1

RUN apt-get update
RUN apt-get install -y wget xz-utils

# Install node
RUN wget https://nodejs.org/dist/$node_version/node-$node_version-linux-x64.tar.xz \
        && tar xf node-$node_version-linux-x64.tar.xz \
        && rm node-$node_version-linux-x64.tar.xz \
        && mv node-$node_version-linux-x64 node \
        && ln -s /node/bin/node /usr/bin/node \
        && ln -s /node/bin/npm /usr/bin/npm \
        && ln -s /node/bin/npx /usr/bin/npx
