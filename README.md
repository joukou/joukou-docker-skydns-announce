Generic SkyDNS Service Announcement Dockerfile for CoreOS
=======================================================
[![Build Status](https://circleci.com/gh/joukou/joukou-docker-skydns-announce/tree/develop.png?circle-token=16be0e437c7d185603a33a2fd2b01bbd153351b1)](https://circleci.com/gh/joukou/joukou-docker-skydns-announce/tree/develop) [![Docker Repository on Quay.io](https://quay.io/repository/joukou/skydns-announce/status "Docker Repository on Quay.io")](https://quay.io/repository/joukou/skydns-announce) [![Apache 2.0](http://img.shields.io/badge/License-apache%202.0-brightgreen.svg)](#license) [![Stories in Ready](https://badge.waffle.io/joukou/joukou-docker-skydns-announce.png?label=ready&title=Ready)](https://waffle.io/joukou/joukou-docker-skydns-announce) [![IRC](http://img.shields.io/badge/IRC-%23joukou-blue.svg)](irc://irc.freenode.org:6667/#joukou)

## Usage

There are two modes of operation, the first is for annoucing the IP address of
a given container's internal `eth0` (virtual) network card:

```
docker run -v /var/run/docker.sock:/var/run/docker.sock -e "SKYDNS_CONTAINER=name-of-container" -e "SKYDNS_INSTANCE=1" -e "SKYDNS_PORT=8080" -e "ETCD_ADDR="172.17.42.1:4001" -e "ETCD_TTL=30"
```

The second is for announcing the IP address of an interface on the CoreOS host
machine itself; i.e. for use with `--net=host`. **Caution:** This tells Docker
to not containerize the container's networking so network-wise the container(s)
live "outside" in the main CoreOS host and have full access to its network
interfaces. This can lead to processes in the container being able to do
unexpected things like [restart your computer](https://github.com/docker/docker/issues/6401).

```
docker run --net=host -e "SKYDNS_IFACE=ens3" -e "ETCD_ADDR=172.17.42.1:4001" -e "ETCD_TTL=30" -e "SKYDNS_NAME=example"
```

In both cases the container process will run, updating etcd, every half of the
etcd TTL.

## Examples

See [`joukou/joukou-fleet`](https://github.com/joukou/joukou-fleet).

## Metrics

[![Throughput Graph](https://graphs.waffle.io/joukou/joukou-docker-skydns-announce/throughput.svg)](https://waffle.io/joukou/joukou-docker-skydns-announce/metrics)

## Contributors

* [Isaac Johnston](https://github.com/superstructor) ([Joukou Ltd](https://joukou.com))
* [Vincent Ambo](https://github.com/tazjin) ([Kivra AB](https://www.kivra.com/))

## License

Copyright &copy; 2014 Joukou Ltd.

Generic SkyDNS Service Announcement Dockerfile for CoreOS is under the Apache 2.0
license. See the [LICENSE](LICENSE) file for details.

[![Analytics](https://ga-beacon.appspot.com/UA-41911221-2/joukou-docker-skydns-announce/readme)](https://github.com/igrigorik/ga-beacon)
