FROM helphi/gitbook:base

RUN npm install gitbook-cli -g &&\
    gitbook fetch 3.2.3 &&\
    rm -rf /tmp/* /var/tmp/*

CMD [ "gitbook", "help" ]