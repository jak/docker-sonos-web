# Docker Container Build of *Sonos-Web*

This Dockerfile builds a docker container version of [Sonos-Web](https://github.com/Villarrealized/sonos-web).

Sonos Web is a browser based controller for your [Sonos](https://www.sonos.com/system) sound system.

Install Sonos Web on a single computer and access and manage your system from any browser on your network.

![Search View](https://user-images.githubusercontent.com/5977736/51435364-fec86800-1c32-11e9-8ca0-a162b1dc1e91.png)

If you need an ARM/Raspberry Pi version, visit [pwt/docker-sonos-web-arm](https://github.com/pwt/docker-sonos-web-arm) which inspired this version.

The docker image name is [`jsixc/sonos-web` on Docker Hub](https://hub.docker.com/r/jsixc/sonos-web).

## Requirements

A working Docker environment. Internet access to pull the Docker image.

## Usage

The container is started as follows:

```
docker run -d \
  --net=host \
  --restart=always \
  --name=sonos-web \
  jsixc/sonos-web
```

To update the container to the latest version, first pull the new image, then stop & restart the container:

```
docker pull jsixc/sonos-web
docker rm --force sonos-web
docker run -d \
  --net=host \
  --name=sonos-web \
  --restart=always \
  jsixc/sonos-web
```

