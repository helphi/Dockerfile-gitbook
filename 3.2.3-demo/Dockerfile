FROM helphi/gitbook:3.2.3-calibre-2

WORKDIR /demo
ADD . ./
RUN gitbook install && rm -rf /tmp/*

EXPOSE 4000

CMD ["gitbook", "serve"]