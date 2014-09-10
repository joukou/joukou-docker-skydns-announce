Generic etcd Service Announcement Dockerfile for CoreOS
=======================================================
[![Build Status](https://circleci.com/gh/joukou/joukou-docker-etcd-announce/tree/develop.png?circle-token=16be0e437c7d185603a33a2fd2b01bbd153351b1)](https://circleci.com/gh/joukou/joukou-docker-etcd-announce/tree/develop) [![Docker Repository on Quay.io](https://quay.io/repository/joukou/etcd-announce/status "Docker Repository on Quay.io")](https://quay.io/repository/joukou/etcd-announce) [![Apache 2.0](http://img.shields.io/badge/License-apache%202.0-brightgreen.svg)](#license) [![Stories in Ready](https://badge.waffle.io/joukou/joukou-docker-etcd-announce.png?label=ready&title=Ready)](https://waffle.io/joukou/joukou-docker-etcd-announce) [![IRC](http://img.shields.io/badge/IRC-%23joukou-blue.svg)](irc://irc.freenode.org:6667/#joukou)

## Usage

```
docker run -e "CONTAINER=riak" -e "SERVICE=riak" -e "TTL=30" quay.io/joukou/etcd-announce
```

## Metrics

[![Throughput Graph](https://graphs.waffle.io/joukou/joukou-docker-etcd-announce/throughput.svg)](https://waffle.io/joukou/joukou-docker-etcd-announce/metrics)

## Contributors

* [Isaac Johnston](https://github.com/superstructor) ([Joukou Ltd](https://joukou.com))
* [Vincent Ambo](https://github.com/tazjin) ([Kivra AB](https://www.kivra.com/))

## License

Copyright &copy; 2014 Joukou Ltd.

Generic etcd Service Announcement Dockerfile for CoreOS is under the Apache 2.0
license. See the [LICENSE](LICENSE) file for details.

[![Analytics](https://ga-beacon.appspot.com/UA-41911221-2/joukou-docker-etcd-announce/readme)](https://github.com/igrigorik/ga-beacon)