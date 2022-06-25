# Ref-docs

## Naming Best Practice

1. [Docker Image Name Convention](https://awstip.com/docker-image-name-convention-951e84dc0a42)

```sh
# Basic
# [image name] = [repository]:[tag]
$ docker build -t ubuntu-with-vim

# Dockerhub
# match the Docker Hub account
$ docker tag ubuntu-with-vim tonylixu/ubuntu-with-vim:v1.9.1
$ docker push tonylixu/ubuntu-with-vim:v1.9.1
```
