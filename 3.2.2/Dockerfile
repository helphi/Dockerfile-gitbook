FROM node:8.1.4-alpine

RUN npm install gitbook-cli -g &&\
    gitbook fetch 3.2.2 &&\
    rm -rf /tmp/*