FROM helphi/gitbook:3.2.3-calibre-3

RUN apt update &&\
    DEBIAN_FRONTEND=noninteractive apt install -y wget --no-install-recommends  &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*


WORKDIR /demo
ADD . ./
RUN mkdir -p /usr/local/share/fonts/win7fonts/ &&\
    wget -q -i fonts -B https://github.com/helphi/fonts/tree/master/win7fonts/ -P /usr/local/share/fonts/win7fonts/
RUN npm install svgexport -g && gitbook install && gitbook pdf && rm -rf /tmp/* /var/tmp/*

EXPOSE 4000

CMD ["gitbook", "serve"]