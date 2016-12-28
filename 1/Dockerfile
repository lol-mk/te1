From ubuntu:14.04
#FROM ubuntu:16.04
RUN apt-get update && apt-get install -y wget libappindicator3-1
RUN wget https://raw.githubusercontent.com/getlantern/lantern-binaries/master/lantern-installer-beta-64-bit.deb -O lantern.deb && \
	dpkg -i lantern.deb
EXPOSE 8787
ENTRYPOINT [ "/usr/bin/lantern", "-headless", "-addr", "0.0.0.0:8787" ]
#ENTRYPOINT [ "/usr/bin/lantern", "--help" ]
