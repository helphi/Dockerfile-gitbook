FROM helphi/gitbook:3.2.3-calibre-3

RUN apt update &&\
    DEBIAN_FRONTEND=noninteractive apt install -y wget --no-install-recommends  &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*


ADD . ./

WORKDIR /usr/local/share/fonts/win7fonts/
RUN wget -q -i fonts1 -B https://github.com/helphi/fonts/tree/master/win7fonts/
RUN wget -q -i fonts2 -B https://github.com/helphi/fonts/tree/master/win7fonts/
RUN wget -q -i fonts3 -B https://github.com/helphi/fonts/tree/master/win7fonts/
RUN wget -q -i fonts4 -B https://github.com/helphi/fonts/tree/master/win7fonts/
RUN wget -q -i fonts5 -B https://github.com/helphi/fonts/tree/master/win7fonts/

WORKDIR /demo
RUN npm install svgexport -g && gitbook install && gitbook pdf && rm -rf /tmp/* /var/tmp/*

EXPOSE 4000

CMD ["gitbook", "serve"]