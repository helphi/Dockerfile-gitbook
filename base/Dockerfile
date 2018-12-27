FROM ubuntu:bionic

ENV LANG=C.UTF-8 TZ=CST-8

RUN apt update &&\
    DEBIAN_FRONTEND=noninteractive apt install -y npm calibre fontconfig fonts-noto-cjk --no-install-recommends &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*