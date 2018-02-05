FROM ubuntu:xenial-20180123

RUN apt update &&\
    apt install -y curl &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*
    
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash - &&\
    apt install -y nodejs &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*

RUN npm install gitbook-cli -g &&\
    gitbook fetch 3.2.3 &&\
    rm -rf /tmp/* /var/tmp/*
    
RUN apt install -y calibre &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*
