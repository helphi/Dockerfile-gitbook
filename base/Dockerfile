FROM ubuntu:bionic-20181112

RUN apt update &&\
    DEBIAN_FRONTEND=noninteractive apt install -y curl calibre fontconfig fonts-noto-cjk --no-install-recommends &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*
    
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash - &&\
    apt install -y nodejs &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*
