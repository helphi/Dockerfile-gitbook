FROM ubuntu:xenial-20180123

RUN sudo apt install -y nodejs calibre &&\
    apt-get autoremove -y && apt-get clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*

RUN npm install gitbook-cli -g &&\
    gitbook fetch 3.2.3 &&\
    rm -rf /tmp/* /var/tmp/*
