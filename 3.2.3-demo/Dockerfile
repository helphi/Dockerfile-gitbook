FROM helphi/gitbook:3.2.3-calibre-3

RUN apt update &&\
    DEBIAN_FRONTEND=noninteractive apt install -y xvfb gconf-service libasound2 libatk1.0-0 libc6 libcairo2 libcups2 libdbus-1-3 libexpat1 libgcc1 libgconf-2-4 libgdk-pixbuf2.0-0 libglib2.0-0 libgtk-3-0 libnspr4 libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxss1 libxtst6 libappindicator1 libnss3 lsb-release xdg-utils wget --no-install-recommends &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*

WORKDIR /demo
ADD . ./
RUN mv fonts-win7-zh /usr/local/share/fonts/
RUN npm install svgexport -g && rm -rf /tmp/* /var/tmp/*
RUN gitbook install && rm -rf /tmp/* /var/tmp/*
RUN gitbook pdf

EXPOSE 4000

CMD ["gitbook", "serve"]