# Install docker ce on centos 7

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

### Installation

```sh
$ sudo yum check-update
$ sudo yum install -y yum-utils device-mapper-persistent-data lvm2
$ sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
$ sudo yum install -y docker
$ sudo systemctl start docker
$ sudo systemctl enable docker
$ sudo systemctl status docker
```

For specific version of docker ce on centos 7

```sh
$ sudo yum list docker-ce --showduplicates | sort –r
$ sudo yum install docker-ce-<VERSION STRING>
```

Install docker-compose

```sh
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.25.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
$ docker-compose --version
```

License
----
MIT

**Free Software, Hell Yeah!**