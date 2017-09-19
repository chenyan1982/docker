FROM     ubuntu:14.04.4
MAINTAINER bitard [dot] michael [at] gmail [dot] com

ENV DEBIAN_FRONTEND=noninteractive \
    NODE_VERSION=8.1.3  \
    NPM_VERSION=5.0.3  \
    IONIC_VERSION=3.5.0 \
    CORDOVA_VERSION=7.0.1
    
# Install basics
RUN apt-get update &&  \
    apt-get install -y git wget curl unzip ruby make && \

    curl --retry 3 -SLO "http://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.gz" && \
    tar -xzf "node-v$NODE_VERSION-linux-x64.tar.gz" -C /usr/local --strip-components=1 && \
    rm "node-v$NODE_VERSION-linux-x64.tar.gz" && \
    npm install -g npm@"$NPM_VERSION" && \
    npm install -g cordova@"$CORDOVA_VERSION" ionic@"$IONIC_VERSION" && \
    npm cache clear --force && \
    gem install sass -v 3.4.25 && \
    
    git config --global user.email "564196013@qq.com" && \
    git config --global user.name "chenyan1982" && \

    ionic start myApp sidemenu

WORKDIR myApp
EXPOSE 8100 35729
CMD ["ionic", "serve"]
