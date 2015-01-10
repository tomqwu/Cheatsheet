#start docker with interact mode
docker run -t -i ubuntu /bin/bash

#remove all containers
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)

#remove all images
docker rmi $(docker images -q)
