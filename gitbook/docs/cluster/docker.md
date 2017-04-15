## Docker
### Installing Docker
Installing docker is fairly easy. Simply run the following command
(The script will ask for your sudo password if required)

    curl -sSL https://get.docker.com/ | sh
    
If it prompts that you haven't yet installed curl, do so first and run the command above it again.  
If it complains about SSL try installing the ca-certificates package.

### Installing Docker-Compose

Docker-Compose makes it easy to setup more complex configurations. It is highly recommended to install it.

```
# Get permissions to install Docker Compose
sudo -i

# Download Docker Compose
curl -L https://github.com/docker/compose/releases/download/1.6.2/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose

# Give it executable rights
chmod +x /usr/local/bin/docker-compose

# return to previous rights
exit
```
> **Note:** the latest release for **docker-compose** is: [![GitHub version](https://badge.fury.io/gh/docker%2Fcompose.svg)](https://badge.fury.io/gh/docker%2Fcompose)

### Managing containers
There are various tools out there to take care of that. However if you just run a few containers it might be easier to just learn a few commands directly from docker.

**The difference between image tags and container names**

Docker can be a bit tricky when it comes to terminology: An **image** is being built from a Dockerfile. This image can have tags specified by option -t.

You then can create a actual **container** from that image that can have a specific name. You can use that name to control the container. e.g. `docker start labs`, `docker stop labs`.

**list all running docker containers**

```sh
docker ps
```

**Manage containers and images**

```shell
# Remove all containers
docker rm $(docker ps -a -q)

# Remove containers that are not currently running
docker rm $(docker ps -q -f status=exited)

# Remove all images
docker rmi $(docker images -q)

# attach current shell/bash to running containers
$ sudo docker attach loving_heisenberg #by Name
```

**Remove all images**

## Docker toolbox
point docker-machine to the right virtualbox instance

```shell
docker-machine env --shell cmd default
```

## Docker Server Setups
### nginx-proxy
[nginx-proxy](https://hub.docker.com/r/jwilder/nginx-proxy/) is a neat way to manage multiple applications on the same server. Docker makes sure that each application can work with its own platform serving stack while the nginx-proxy docker container makes sure that the different containers all get their related traffic.


# Links
Some commands:  
http://stackoverflow.com/questions/17665283/how-does-one-remove-an-image-in-docker
