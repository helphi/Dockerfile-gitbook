FROM node:9.4.0

RUN npm install gitbook-cli -g &&\
    gitbook fetch 3.2.3 &&\
    rm -rf /tmp/*

RUN sudo -v &&\
    wget -nv -O- https://download.calibre-ebook.com/linux-installer.py |\
    sudo python -c "import sys; main=lambda:sys.stderr.write('Download failed\n'); exec(sys.stdin.read()); main()"
