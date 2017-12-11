FROM node:8.1.4

RUN npm install gitbook-cli -g &&\
    gitbook fetch 3.2.2 &&\
    rm -rf /tmp/*

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y calibre &&\
    rm -rf /var/lib/apt/lists/*