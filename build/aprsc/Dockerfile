FROM debian:buster-slim

RUN apt-get update && \
    apt-get install -y build-essential \
    debhelper \
    libc6 \ 
    zlib1g \
    adduser \
    libcap2-bin \
    libwww-perl \
    libjson-xs-perl \
    libevent-dev \
    git \
    lsb-release

RUN git clone https://github.com/hessu/aprsc && \
    cd aprsc/src && \
    ./configure && \
    make make-deb && \
    cd .. && \
    apt-get install ./*.deb

CMD service aprsc start && tail -F /opt/aprsc/logs/aprsc.log
