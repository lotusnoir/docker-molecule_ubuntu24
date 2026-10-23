
# Docker Image with Ubuntu 24 base image

This repo was created in order to test ansible roles with molecule.

## Build it locally

### Build

  docker build -t ubuntu24img .

### Run

  docker run -d --name ubuntu24con \
  --privileged \
  --cgroupns=host \
  --volume=/sys/fs/cgroup:/sys/fs/cgroup:rw ubuntu24img

### Test

  docker exec ubuntu24con systemctl is-system-running --wait

### Explore

  docker exec -it ubuntu24con bash

## Use it from dockerhub

    https://hub.docker.com/repository/docker/lotusnoir/ansible_molecule_test_images:ubuntu24
