FROM debian:buster-slim

RUN apt update && \
    apt install -y build-essential \
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
    make make-deb -j4 && \
    cd .. && \
    apt install ./*.deb

CMD service aprsc start && tail -F /opt/aprsc/logs/aprsc.log
