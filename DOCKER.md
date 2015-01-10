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
```bash
docker run -d -P --name web -v /src/webapp:/opt/webapp training/webapp python app.py
```
