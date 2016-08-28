FROM selenium/node-firefox:2.53.0
MAINTAINER Heiko Bornholdt <heiko@bornholdt.it>

RUN apt-get update -qqy \
  && apt-get -qqy install \
    fonts-wqy-zenhei fonts-arphic-bkai00mp fonts-arphic-bsmi00lp fonts-arphic-gbsn00lp fonts-arphic-gkai00mp fonts-arphic-ukai fonts-arphic-uming fonts-cwtex-fs fonts-cwtex-heib fonts-cwtex-kai fonts-cwtex-ming fonts-cwtex-yen \
  && rm -rf /var/lib/apt/lists/*

USER root

#====================================
# Scripts to run Selenium Standalone
#====================================
COPY entry_point.sh /opt/bin/entry_point.sh
RUN chmod +x /opt/bin/entry_point.sh

USER seluser

EXPOSE 4444
