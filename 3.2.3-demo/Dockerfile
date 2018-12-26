FROM helphi/gitbook:3.2.3-calibre

ENV LANG=C.UTF-8 TZ=CST-8

RUN apt update &&\
    DEBIAN_FRONTEND=noninteractive apt install -y fontconfig fonts-noto-cjk --no-install-recommends &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*

RUN gitbook install && rm -rf /tmp/*

EXPOSE 4000

CMD ["gitbook", "serve"]