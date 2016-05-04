FROM debian:latest

RUN apt-get update
RUN apt-get -y install wget

RUN wget https://bitcoin.org/bin/bitcoin-core-0.12.1/bitcoin-0.12.1-linux64.tar.gz
RUN tar xzf bitcoin-0.12.1-linux64.tar.gz
RUN install -m 0755 -o root -g root -t /usr/local/bin bitcoin-0.12.1/bin/*

VOLUME ['/data']

EXPOSE 8333

CMD ["bitcoind", "-datadir=/data", "-disablewallet", "-server"]
