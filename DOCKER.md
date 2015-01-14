#start docker with interact mode
```bash
docker run -t -i ubuntu /bin/bash
```

#remove all containers
```bash
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```

#remove all images
```bash
docker rmi $(docker images -q)
```
# mount a host directory
URL: https://docs.docker.com/userguide/dockervolumes/
```bash
docker run -i -t -v /data/okapi:/home/okapi/data canadatom/okapi-docker-file /bin/bash
```

# start and attach a stopped container
## list all containers
```bash
docker ps -a 
```

## start the container with id
```bash
docker start [container_id]
```

## attach the container
```bash
docker attach [container_id]
```
