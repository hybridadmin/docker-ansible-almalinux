# AlmaLinux Docker Images with ansible and systemd

![Build](https://github.com/hybridadmin/docker-ansible-almalinux/workflows/Build/badge.svg?branch=main) ![Docker Pulls](https://img.shields.io/docker/pulls/hybridadmin/ansible-almalinux)

> AlmaLinux Docker images to be used for testing ansible playbooks and roles.

## Quick reference

- Maintained by: [hybridadmin](https://github.com/hybridadmin)
- Where to get help: [The Docker Community Forums](https://forums.docker.com/), [Docker Community on Slack](https://dockr.ly/slack) or [Stack Overflow](https://stackoverflow.com/search?tab=newest&q=docker)
- Where to file issues: [(issue tracker)](https://github.com/hybridadmin/docker-ansible-almalinux/issues) include the `docker` tag
- Supported Arch(s): [(more info)](https://github.com/docker-library/official-images#architectures-other-than-amd64) `amd64`

## Supported tags and respective `Dockerfile` links

- [`9`](https://github.com/hybridadmin/docker-ansible-almalinux/tree/main/9/Dockerfile)
- [`latest`, `8`](https://github.com/hybridadmin/docker-ansible-almalinux/tree/main/8/Dockerfile)

## How to Build the image

1. Install docker
   - [Linux](https://docs.docker.com/engine/install/)
   - [Windows](https://docs.docker.com/docker-for-windows/install/)
2. Clone the repo `git clone https://github.com/hybridadmin/docker-ansible-almalinux.git`
3. `cd` into the directory
4. Run `docker build -t ansible-almalinux .`

## How to use this image

Pull the image using the following command:

```console
docker pull hybridadmin/ansible-almalinux:latest
```

Run a container using the image with the following command:

```console
docker run -d --privileged -v /sys/fs/cgroup:/sys/fs/cgroup:ro hybridadmin/ansible-almalinux:latest
```

Use ansible inside the container:

```console
docker exec --tty [container_id] env TERM=xterm ansible --version
docker exec --tty [container_id] env TERM=xterm ansible-playbook /path/to/playbook.yml --syntax-check
```

Connect to the container:

```console
docker exec -it [container_id] /bin/bash
```
