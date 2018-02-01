FROM node:9.4.0

RUN npm install gitbook-cli -g &&\
    gitbook fetch 3.2.3 &&\
    rm -rf /tmp/*

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y calibre &&\
    rm -rf /var/lib/apt/lists/*
