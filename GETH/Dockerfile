FROM ubuntu:18.04


RUN apt-get update

RUN apt-get install -y software-properties-common

RUN add-apt-repository -y ppa:ethereum/ethereum

RUN apt-get update

RUN apt-get install -y ethereum

RUN mkdir /ethereum

ADD genesis.json /ethereum

EXPOSE 8545

EXPOSE 30303


CMD ["geth","--datadir /ethereum","init /ethereum/genesis.json"]

ENTRYPOINT [ "geth","--datadir","/ethereum","-rpc","-nodiscover","--networkid","1500"]

