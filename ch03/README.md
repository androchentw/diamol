# ch03 

```sh
# 3.1
docker image pull diamol/ch03-web-ping
docker container run -d --name web-ping diamol/ch03-web-ping  # -d = --detach
docker container logs web-ping
docker rm -f web-ping
docker container run --env TARGET=google.com diamol/ch03-web-ping

# 3.2
cd ch03/exercises/web-ping

# 3.3
docker image build --tag web-ping .   # -t = --tag, set friendly image name
docker image ls 'w*'
docker container run -e TARGET=docker.com -e INTERVAL=5000 web-ping

# 3.4
docker image history web-ping
docker image ls
docker system df

# 3.5
# change code in ch03/exercises/web-ping to check docker cache behaviour
docker image build -t web-ping:v2 .
# optimize rule: put less changed part on above to utilize cache
cd ../web-ping-optimized
docker image build -t web-ping:v3 .

# 3.6 lab
docker container run -it --name ch03lab diamol/ch03-lab
echo Andro >> ch03.txt 
exit
docker container commit ch03lab ch03-lab-soln
docker container run --name andro_lab_ch03 ch03-lab-soln cat ch03.txt

docker container logs ch03lab 
docker container diff ch03lab
docker container ls --all --quiet
docker container logs andro_lab_ch03
docker image history diamol/ch03-lab
docker image history ch03-lab-soln
```
