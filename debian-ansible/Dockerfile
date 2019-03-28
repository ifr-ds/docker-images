FROM ifrds/debian:latest
MAINTAINER Tomasz Tylec <ttylec@ifesearch.pl>

RUN apt-get install --no-install-recommends -yq gnupg2 dirmngr && \
    apt-get autoremove -y && \
    rm -rf /var/lib/apt/lists/*.deb

RUN echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main" >> /etc/apt/sources.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367 && \
    apt-get update && \
    apt-get install --no-install-recommends -yq ansible && \
    apt-get autoremove -y && \
    rm -rf /var/lib/apt/lists/*.deb