# Docker Python Images

Base Python Docker images.

## What's Included

* [docker-bootstrap](https://github.com/articulate/docker-bootstrap) entrypoint
  for loading environment variables from Consul and Vault.
* [secrets](https://github.com/articulate/docker-bootstrap/blob/main/scripts/docker-secrets)
  to load Docker secrets as environment variables.
* [install_packages](https://github.com/articulate/docker-bootstrap/blob/main/scripts/install_packages)
  to install apt packages.
* [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
  for interacting with AWS services.

## Tags

> 🌟 recommended image

* __articulate/python:3.14__ 🌟
  > TODO: versions for pytorch, torchvision for 3.14 need confirmation
* __articulate/python:3.13__ 🌟
  > pytorch, torchvision for 3.13 not yet available
* articulate/python:3.12
* articulate/python:3.12-pytorch
* articulate/python:3.11

## Creating a new image

The easiest way to create a new image is to copy an existing one and change the
base image. If creating from scratch, the images need the following:

* Everything listed in [What's included](#whats-included)
* `make` for internal tooling.
* A _service_ user and group with a GID and UID of 1001. This should be the default
  user.
* A _/service_ directory as the default working directory.
