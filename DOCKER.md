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

# stop a container
```
ctrl+d
```

# start a container
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

## list all containers name and IP
```
docker ps | tail -n +2 | while read -a a; do name=${a[$((${#a[@]}-1))]}; echo -ne "$name\t"; docker inspect $name | grep IPAddress | cut -d \" -f 4; done
```
