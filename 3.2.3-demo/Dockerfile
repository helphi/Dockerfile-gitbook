FROM helphi/gitbook:3.2.3-calibre-3

WORKDIR /demo
ADD . ./
RUN gitbook install && rm -rf /tmp/* /var/tmp/*

EXPOSE 4000

CMD ["gitbook", "serve"]