# Docker Notes

**launches the image 'hello-world'**  
docker run hello-world

**lists all images locally available**  
docker images

**shows list of running containers (and ones that 'were' on)**  
docker ps --all

**exit**  
exits bash

**starts the docker image with a container_id**  
docker start -I ab0e37214358  
**-without the -i in the command it won't open bash**  
**-to open bash after running without -I you need to run, docker attach ab0e37214358**

**stop the container**  
docker stop MyWebServer

**see the port # for container 'MyWebServer'**  
docker port MyWebServer

**launch image. -P parameter is to publish all exposed ports to random ports**  
docker run -d --name MyWebServer -P httpd 60debd0d57bf292b0c3f006e4e52360feaa575e45ae3caea97637bb26b490b10

**deletes (rm) all images locally**  
docker system prune

**stops and removes containers**  
docker-compose down -v

**stop docker container**  
docker stop <container id>

**remove docker container**  
docker rm <container id>

**runs docker compose in detached mode**  
docker-compose up -d

**-f parameter tells it to don't use the default name Dockerfile**  
docker-compose -f prod.yml up

**command line in the docker container**  
docker exec -it <container id> bash

**makes it so the docker container can collect static files for nginx.**  
docker-compose -f prod.yml run --rm app python manage.py collectstatic

**docker exec -it <container name> /bin/bash**  
bash into directory

**docker cp <containerId>:/file/path/within/container /host/path/target**  
copy file to host from docker container

**fake migration**  
python3 manage.py migrate app_name migration_number --fake  
ex: python3 manage.py migrate events 0040 --fake