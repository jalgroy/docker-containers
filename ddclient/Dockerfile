FROM debian:latest
MAINTAINER Joakim Algrøy <joakimalgroy@gmail.com>

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -yq ddclient

VOLUME /config

ENTRYPOINT /usr/sbin/ddclient -daemon -file /config/ddclient.conf && tail -F /var/log/daemon.log
