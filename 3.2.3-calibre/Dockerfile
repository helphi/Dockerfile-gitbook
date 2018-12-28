FROM ubuntu:bionic

ENV LANG=C.UTF-8 TZ=CST-8

RUN apt update &&\
    DEBIAN_FRONTEND=noninteractive apt install -y calibre --no-install-recommends  &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*

RUN apt update &&\
    DEBIAN_FRONTEND=noninteractive apt install -y fonts-noto-cjk --no-install-recommends &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*

RUN apt update &&\
    DEBIAN_FRONTEND=noninteractive apt install -y ca-certificates nodejs npm &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*

RUN npm install gitbook-cli -g &&\
    gitbook fetch 3.2.3 &&\
    rm -rf /tmp/* /var/tmp/*

CMD [ "gitbook", "help" ]