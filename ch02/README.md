# ch02 

```sh
# 2.1
docker version
docker-compose version
docker container run diamol/ch02-hello-diamol

# 2.3
docker container run --interactive --tty diamol/base

docker container ls
# <short container id>: 77
docker container top 77 # Display the running processes of a container
docker container logs 77  # Fetch the logs of a container
docker container inspect 77  # Return low-level information on Docker objects

# 2.4
docker container ls -all
docker container run --detach --publish 8088:80 diamol/ch02-hello-diamol-web  

docker container ls
docker container stats c9c  # Display a live stream of container(s) resource usage statistics

docker container rm --force $(docker container ls --all --quiet)
```
