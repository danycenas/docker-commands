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

**How to create a container?**
```java
docker container ps -a
/* List all container (initiated or detained)  */

docker run -it ubuntu
/* Created container name by default */

docker run -it --name containerUbuntu ubuntu
/* Created container name assigned */

docker run -it --name containerUbuntu -d ubuntu
/* Start a container in detached mode */

docker start <CONTAINER-NAME OR CONTAINER-ID>
/* Start container */

docker stop <CONTAINER-NAME OR CONTAINER-ID>
/* Stop container */

docker port <CONTAINER-NAME OR CONTAINER-ID>
/* List port mappings or a specific mapping for the container */

docker inspect <CONTAINER-NAME OR CONTAINER-ID>
/* Container detail  */

docker logs <CONTAINER-NAME OR CONTAINER-ID>
/* Fetch the logs of a container */

docker rm <CONTAINER-NAME OR CONTAINER-ID>
/* Delete container */
```

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
