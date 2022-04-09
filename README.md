## About

Companion repository to the [CrateDB and Prometheus for long-term metrics storage]
tutorial, based on Docker and Docker Compose.


## Details

The setup has been verified with Docker 20.10.14 and Docker Compose v2.3.3
on Debian Linux, Ubuntu and macOS.

Please note that the Docker Compose configuration is completely ephemeral, no
data will be persisted. After shutting down the containers, all data will be
gone.

It is just a demo setup, a real production installation will probably use a
more advanced setup of this software stack.


## Setup

### Prerequisites

The tutorial is based on Docker, so let's install the corresponding software
first.

```shell
# Debian Linux
# Setup the package repository by following https://docs.docker.com/engine/install/debian/.
apt install --yes git docker-ce containerd.io docker-ce-cli docker-compose-plugin

# macOS
brew install git
brew install --cask docker
```

### Services
```shell
git clone https://github.com/crate-workbench/cratedb-prometheus-demo
cd cratedb-prometheus-demo
docker compose pull
docker compose up
```


## Usage

HTTP URLs for services:

- CrateDB: http://localhost:4200/
- Prometheus: http://localhost:9090/

You can also visit the `/metrics` endpoint of the CrateDB Prometheus Adapter at
http://localhost:9268/metrics.


[CrateDB and Prometheus for long-term metrics storage]: https://community.crate.io/t/cratedb-and-prometheus-for-long-term-metrics-storage/1012
