ARG NODE_VERSION

FROM node:$NODE_VERSION

ARG HUGO_VERSION=0.91.0

RUN apt-get update && apt-get install -y wget

# https://github.com/gohugoio/hugo/releases/download/v0.91.0/hugo_0.91.0_Linux-64bit.tar.gz
RUN wget https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_${HUGO_VERSION}_Linux-64bit.tar.gz && \
    tar -xf hugo_${HUGO_VERSION}_Linux-64bit.tar.gz -C /usr/local/bin && \
    hugo version && rm hugo_${HUGO_VERSION}_Linux-64bit.tar.gz
    
RUN wget -q -O - https://raw.githubusercontent.com/canha/golang-tools-install-script/master/goinstall.sh | bash
