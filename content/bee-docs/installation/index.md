---
title: 'Installation'
weight: 2
summary: "How to install client code to run a node."
alias: "/bee-docs/installation.html"
---

## Supported platforms

The client can be installed on MacOS and various Linux flavors.

## Installing the Bee binary
At every official release, we release the binary files of our software. You can download them by navigating to [releases](https://github.com/ethersphere/bee/releases).

A convenient way to download the binary is:

```sh
wget https://github.com/ethersphere/bee/releases/latest/download/bee-darwin-amd64 -O /usr/local/bin/bee
chmod +x /usr/local/bin/bee
```

Please change the last part of the url (`bee-darwin-amd64`), if you are not on a `darwin-amd64` system. A list of supported systems is available at [releases](https://github.com/ethersphere/bee/releases).

## Installing Bee with Docker
Bee can be run as a docker container.

Download bee as a docker container by running:

`docker pull ethersphere/bee:<version>`

Where version is the release which you want to download (see [releases](https://github.com/ethersphere/bee/releases)).

Please see [Dockerhub](https://hub.docker.com/r/ethersphere/bee) for more information.

## Installation from source
<!-- https://raw.githubusercontent.com/ethersphere/bee/master/README.md -->

Prerequisites for installing Bee from source are:

- Go - download the latest release from [golang.org](https://golang.org/dl),
- git - download from [git-scm.com](https://git-scm.com/) or install with your package manager,
- make.

1) Clone the repository:
```sh
git clone https://github.com/ethersphere/bee
cd bee
```

2) Use `git` to find the latest release:
```sh
git describe --tags
```

3) Checkout the latest release:

```sh
git checkout <name_of_latest_tag>
```

4) Build the binary and move the binary to your path:

```sh
make binary
cp dist/bee /usr/local/bin/bee
```

5) You should now be able to run the `bee` command, which you can verify by running:
```sh
bee version
```

Which should return the version number of the Bee you are running.