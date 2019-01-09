## Docker Images

**How to use a imagen?**
```java
docker images
/* List all images */

docker pull debian
/* Download a imagen */

docker pull debian:8
/* Download a imagen with specific tag */
```

## Docker Containers

**How to create/delete a container?**
```java
docker container ps
/* List all container initiated */
-a
-l

docker run -it ubuntu
/* Created container name by default */

docker run -it --name containerUbuntu ubuntu
/* Created container name assigned */

docker run -it --name containerUbuntu -d ubuntu
/* Start a container in detached mode */
-p
-m "500mb"
-cpuset-cpus 0-1
--rm


docker cp index.html apache:/tmp
docker cp apache:/va/httpd

docker rm <CONTAINER-NAME OR CONTAINER-ID>
/* Delete container */
```

**How to start/stop a container?**
```java
docker start <CONTAINER-NAME OR CONTAINER-ID>
/* Start container */

docker stop <CONTAINER-NAME OR CONTAINER-ID>
/* Stop container */
```

**Another options from container**
```java
docker exec -it containerDebian bash
docker exec -it containerDebian -c "cat /etc/os-release"
/* Access a started container */

docker port <CONTAINER-NAME OR CONTAINER-ID>
/* List port mappings or a specific mapping for the container */

docker inspect <CONTAINER-NAME OR CONTAINER-ID>
/* Container detail  */

docker logs <CONTAINER-NAME OR CONTAINER-ID>
/* Fetch the logs of a container */
-f

docker stats <CONTAINER-NAME OR CONTAINER-ID>
/* Display a live stream of container(s) resource usage statistics */

docker commit <CONTAINER-NAME OR CONTAINER-ID> <IMAGE_NAME>

docker info
/* Directory today */
```

**Docker Network**
```java
docker network ls
/* List all network */

docker network create <NETWORK_NAME>
/* Using driver bridge */

docker network inspect <NETWORK_NAME>
/* Inspect created network */

docker network -d bridge --subnet <IP-0>/24 --gateway <IP-1> <NETWORK_NAME>
/* Assign gateway and subnet */

docker run --network <NETWORK_NAME> -it --name containerDebian debian
docker run --network <NETWORK_NAME> --ip <IP-X> -it --name containerDebian debian
/* Create container with created network */

docker network connect <NETWORK_NAME> <CONTAINER_NAME>
/* Connect containers in different networks */

docker network disconnect <NETWORK_NAME> <CONTAINER_NAME>
/* Disconnect a container from a network */

docker network rm <CONTAINER_NAME>
/* Delete created network */

docker network rm <CONTAINER_NAME>
/* Assign IP to a container */

docker run --network host -it --name containerDebian debian
/* Create container in host network */

docker run --network none -it --name containerDebian debian
/* Create container in host network */
```

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
