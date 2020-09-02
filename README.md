# aprsc-docker
Dockerized APRSC using Debian Buster

This is a Dockerized version of hessu.fi/aprsc. 
APRSC is an APRS-IS server implementation written in C. 
APRSC can be used to create personal or private APRS network, instead of using the global APRS-IS network.

## Installation

Before running the docker commands, configure the APRSC service by editting the aprsc.conf
```
# nano ./config/etc/aprsc.conf
```

Fill out your server name, pass code (generate one from apps.magicbug.co.uk/passcode) and your information. 
Make sure to read all the configuration files properly and once you're done save the changes.
Start the docker-container by using these following commands:

```
$ docker-compose up -d
```
